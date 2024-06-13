//số hoàn hảo
for (int i = 1; i <= a / 2; i++) {
 if (a % i == 0){
 sum += i;
 }
}
if (sum == a) {
 Console.WriteLine("\n{0} là số hoàn hảo.", a);
 } else {
 Console.WriteLine("\n{0} không phải là số hoàn hảo.", a);
 }