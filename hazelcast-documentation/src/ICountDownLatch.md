

## ICountDownLatch


CountdownLatch: Concurrent activity gate-keeping

The java.util.concurrent.CountDownLatch was introduced in Java 1.5 and is a syn- chronization aid that makes it possible for threads to wait until a set of operations, being performed by one or more threads to complete. Very simplistically; a Count- DownLatch could be seen as a gate containing a counter. Behind this gate, threads can wait till the counter reaches 0. In my experience CountDownLatches often are used when you have some kind of processing operation, and one or more threads need to wait till this operation completes so they can execute their logic. Hazelcast also contains a CountDownLatch; the org.hazelcast.core.ICountDownLatch.


public static void main(String[] args) throws Exception { HazelcastInstance hz = Hazelcast.newHazelcastInstance(); ICountDownLatch latch = hz.getCountDownLatch("latch"); System.out.println("Waiting");


