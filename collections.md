### Collections
- `Collection` java.util paketinde yer alirlar.
- `java.util.Collection`, `java.util.List`, `java.util.Set`, `java.util.Map`, `java.util.Queue`
- Ordered & Unordered
   - **ordered** yapida , elemanlar belli bir sirada tutulur.
   - `java.util.ArrayList` **ordered** bir yapiya sahiptir.
   - elemanlar ekledigimiz sirada tutulur. **index based**
   - `java.util.HashMap` / `java.util.HashSet` ise **unordered** bir yapiya sahiptir.
   - elemanlar ekledigimiz sirada TUTULMAZ.
- Sorted & UnSorted
   - elemanlarin sirali olmasi ozelligi.
   - `TreeSet` ve `TreeMap` , sorted ozellige sahiptir.
   - **natural order** -> `alfabetik` siralama , ya da `numerik` siralama mantigi.
   - kendimiz bir `Person` sinifi olusturdugumuzda ve objeler olusturdugumuzda neye gore kime gore siralanacak -> bu durumda `Comparable` , `Comparator` gibi interfaceleri kullaniriz.
#### List   `public interface List<E> extends Collection<E>`
- `List` duplicate elemana izin verir , elemanlar **index based** olarak tutulur.
- `java.util.ArrayList`, `java.util.LinkedList`, `java.util.Vector`
- `ArrayList` , *random access* ve *iteration* soz konusu oldugunda daha **hizli** calisir.
- `LinkedList` , *ekleme/cikartma add/delete* islemi bol miktar kullaniliyorsa daha **verimli** olacaktir.
- `LinkedList` ayni zamanda `Queue` interfacesini implement etmektedir.
- Vector, javanin 1.2 versiyonunda beri varidir.metotlari `synchronized` ozellige sahiptir. **thread safetir**.daha yavas calisir.
#### Set  `public interface Set<E> extends Collection<E>`
- `Set` -> *kume* demek.**Duplicate** elemana izin vermez!
- `java.util.HashSet`, `java.util.LinkedHashSet`, `java.util.TreeSet`
- `HashSet` -> *unordered* bir yapiya sahiptir.
  - `LinkedHashSet` -> *ordered* bir yapiya sahiptir.elamanlar eklenildigi sirada TUTULUR!
- `TreeSet` -> elemanlar *sorted* sekilde tutulur!
#### Map  `public interface Map<K, V>`
- `K` -> `key` & `V` -> `value` cifti seklinde tutulur.
- `key` unique olmak *zorundadir*.`value` unique olmak *zorunda degildir*.
- `java.util.HashMap` -> unordered bir yapiya sahiptir. elemanlar eklenildigi sirada tutulmaz.
  - `HashMap` `null key`'e izin verir. `value` olarak da `null` eklenebilir.
- `java.util.Hashtable`
  - `Vector` sinif gibi javanin eski versiyonlarindan beri vardir. metotlari `synchronized` ozellik gosterir. 
  - `Hashtable` , **null key ya da value** eklenmesine izin vermez!
- `java.util.TreeMap` *Sorted* ozellige sahiptir.
  - elemanlari sirali sekilde tutulur. key e gore sirali sekilde.!
#### Genel
- `Arrays.asList` ile bir arrayden List olusturdugumuzda eleman **eklemize** izin vermez! 
- `collectionlarin` elemanlari **obje**dir. primitive eleman tutmazlar!
- **Code to Interface**  `List<Integer> numbers3 = new ArrayList<>(); `
  - sol taraf interface -> List
  - sag taraf implement eden class ->ArrayList
  - esneklik acisindan dogru bir yaklasimdir. `numbers3 = new LinkedList<>();` 
- `Set` duplicate elemana izin vermez!
  - `equals` ve `hashcode` metodunu override ettigimizde bu durumda equals true olacagi icin duplicate eleman olurlar.eger override edilmezse java bunlarin duplicate oldugunu anlamaz. java acisindan duplicate degildir cunku equalsu true degildir eger override edilmezse.. 