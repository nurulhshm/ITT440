import java.io.*;
import java.net.*;

public class Client{
public static void main(String[] args) throws IOException {

Socket s = null;


try{
    System.out.println("connecting to host...");
    s = new Socket("dagobah", 6464);
}catch (UnknownHostException e) {
    System.err.println("Can't connect");
    System.exit(1);
}
System.out.println("Connected to host");


s.close();
}
}

