protokuł kominukacyjny warstwy sieciowek (network) modelu osi.
Zapewnia komunikację end to end a nie point to point tak jak ethernet

    End to end indicates a communication happening between two applications (maybe you and your friend using Skype). It doesn't care what's in the middle, it just consider that the two ends are taking with one another. It generally is a Layer 4 (or higher) communication
    
    Point to point is a Layer 2 link with two devices only on it. That is, two devices with an IP address have a cable going straight from a device into the other. A protocol used there is PPP, and HDLC is a legacy one.
    
    Hop by Hop indicates the flow the communication follows. Data pass through multiple devices with an IP address, and each is genetically named “hop”. Hop by Hop indicates analyzing the data flow at layer 3, checking all devices in the path