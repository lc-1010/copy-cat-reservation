

## Service interface

```proto

enum ReservationStatus {
    UNKONOW =0;
    PENDING = 1;
    CONFIRMED = 2;
    BLOCKED = 3;
}

enum ReservationUpdateType {
    UNKNOW =0;
    CRATE = 1;
    UPDATE = 2;
    DELETE = 3;
}

message Reservation {
    string id =1;
    string user_id = 2;
    ReservationStatus status = 3;// for user show type infomeration

    // resource reservation window
    string resource_id =4;
    google.protobuf.Timestamp start = 5;
    google.protobuf.Timestamp end = 6;

    //exta note
    string note = 7;
}

message ReserveRequest {
    Reservation reservation =1;
}
message ReserveResponse {
    Reservation reservation =1;
}

message ConfirmRequest {
    string id =1;
}

message ConfirmResponse{
    Reservation reservation =1;
}

//
message UpdateRequest {
    string note =2;

}
message UpdateResponse{
    Reservation reservation =1;
}
message CanceRequest {
    string id = 1;
}
message CanceResponse{
    Reservation reservation = 1;
}
message GetRequest {
    string id =1;
}
message GetResponse {
     Reservation reservation = 1;

}
message QueryRequest {
    string resource_id =1;
    string user_id =2;
    //user status to filter  results.if unknow return all reservations
    ReservationStatus status =3;
    google.protobuf.Timestamp start =4;
    google.protobuf.Timestamp end = 5;

}

service ReservationService {
    rpc resrve(ReserveRequest) returns (ReserveResponse);
    rpc confirm(ConfirmRequest) returns (ConfirmResponse);
    rpc update(UpdateRequest) returns (UpdatedResponse);
    rpc cancel(CancelRequest) returns (CancelResponse);
    rpc get(GetRequest) returns (GetResponse);
    rpc query(QueryRequest) returns (stream Reservation);//
    //
    rpc listen(ListenRequest) returns (stream Reservation);
}

```

## Database schema

- 数据库选型
  - 迁移成本高
  - 并发情况下的冲突，锁

use postgres as the database. schema
```sql
CRATE SCHEMA rsvp;

CRATE TABLE rsvp.reservation

```
