<!DOCTYPE html>
<html>
<head>
  <title>Protobuf in HTML</title>
</head>
<body>
  <h1>Protocol Buffers in HTML</h1>
  <script type="module">
    import * as jspb from './user_pb.js';
    const user = new jspb.User();
    user.setName("Alice");
    user.setAge(25);
    const bytes = user.serializeBinary();
    console.log("Serialized:", bytes);
    const user2 = jspb.User.deserializeBinary(bytes);
    console.log("Deserialized Name:", user2.getName());
    console.log("Deserialized Age:", user2.getAge());
  </script>
</body>
</html>
