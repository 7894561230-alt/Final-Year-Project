# Final-Year-Project
long accelX, accelY, accelZ; 
// For Getting acceleration
float gForceX, gForceY, gForceZ;
long gyroX, gyroY, gyroZ; 
// For Tilt Angle
float rotX, rotY, rotZ;
record AccelRegisters();
record GyroRegisters();
print Data();

gForceX = (accelX / 16384.0);
gForceY = (accelY / 16384.0);
gForceZ = accelZ / 16384.0;

if ((rotY > 60 || rotY <-60) || (rotX > 60 || rotY <-60) )
//&& (gForceX > 0.1 || gForceX < -0.1))
{
// Keep reading from Arduino Serial Monitor and send to HC-05
Int message = "1";
// (Serial.write("1"));
Serial.write("1");
Serial.print("\n");
