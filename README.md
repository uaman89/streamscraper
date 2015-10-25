import java.net.URI;
import java.util.List;
import net.moraleboost.streamscraper.Stream;
import net.moraleboost.streamscraper.Scraper;
import net.moraleboost.streamscraper.scraper.IceCastScraper;
 
public class
 
Harvester{
   public static void main(String[] args)throws Exception
   {
        Scraper scraper =newIceCastScraper();    
   List<Stream> streams = scraper.scrape(new URI("http://host:port/"));
       for(Stream stream: streams){
            System.out.println("Song Title: "+ stream.getCurrentSong());              
            System.out.println("URI: "+ stream.getUri());    
       }
  }
}
