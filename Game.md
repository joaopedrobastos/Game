import java.awt.Canvas;

/**
 *
 * @author João Pedro
 */
public class Game extends Canvas implements Runnable{
    
    private boolean running = false;
    private Thread thread;
    
    public synchronized void start(){
        if(running)
            return;
        
        running = true;
        thread = new Thread(this);
        thread.start();
    }
    
    @Override
    public void run() {
        
        long lastTime = System.nanoTime();
        double amoutOfTicks = 60.0;
        
        
        
        
    }
    
    
    public static void main(String args[]){
        
        new Window(800, 600, "Phanton Platform Game", new Game());
        
    }
}
