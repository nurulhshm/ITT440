import java.net.*;
import java.io.*;
import java.util.*;


public class server{
public static void main(String[] args) throws IOException{


ServerSocket serverSocket = null;
try{
    serverSocket = new ServerSocket(6464);
}catch (IOException e){
    System.err.println("fail to start server");
    System.exit(1);
}
System.out.println("Server started : )");



Socket clientSocket = null;
try{
    System.out.println("waiting for a client...");
    clientSocket = serverSocket.accept();
} catch (IOException e) {
    System.out.println("fail can't accept client connection");
    System.exit(-1);
}
System.out.println("client connected");


clientSocket.close();
serverSocket.close();
}