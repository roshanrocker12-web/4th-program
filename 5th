import java.util.Scanner;

public interface SmartDevice {
    void turnOn();
    void turnOff();

    // Main method inside interface - so "java SmartDevice" will work
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine().trim());

        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().trim().split("\\s+");
            String deviceName = parts[0];
            String action = parts[1];

            SmartDevice device = null;

            if (deviceName.equals("Fan")) {
                device = new SmartFan();
            } else if (deviceName.equals("Light")) {
                device = new SmartLight();
            } else if (deviceName.equals("AC")) {
                device = new SmartAC();
            } else {
                continue;
            }

            if (action.equalsIgnoreCase("ON")) {
                device.turnOn();
            } else {
                device.turnOff();
            }
        }
        sc.close();
    }
}

class SmartFan implements SmartDevice {
    public void turnOn() {
        System.out.println("Smart Fan is turned ON");
    }
    public void turnOff() {
        System.out.println("Smart Fan is turned OFF");
    }
}

class SmartLight implements SmartDevice {
    public void turnOn() {
        System.out.println("Smart Light is turned ON");
    }
    public void turnOff() {
        System.out.println("Smart Light is turned OFF");
    }
}

class SmartAC implements SmartDevice {
    public void turnOn() {
        System.out.println("Smart AC is turned ON");
    }
    public void turnOff() {
        System.out.println("Smart AC is turned OFF");
    }
}
