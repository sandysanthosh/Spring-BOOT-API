# Spring-BOOT-API


#### In Spring Boot, you can convert a List to an ResponseEntity<List> using the ResponseEntity class. Here's an example of how you can do it:

```

@GetMapping("/users")
public ResponseEntity<List<User>> getAllUsers() {
    List<User> userList = userService.getAllUsers();
    if(userList.isEmpty()) {
        return new ResponseEntity<>(HttpStatus.NO_CONTENT);
    }
    return new ResponseEntity<>(userList, HttpStatus.OK);
}


```
