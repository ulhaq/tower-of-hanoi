# Tower of Hanoi
The formula for calculating the number of minimum moves it takes to complete a Tower of Hanoi is:
<strong>M<sub>n</sub> = 2<sup>n</sup> - 1</strong>
where n is the number of discs

## Implementation of a recursive algorithm
```
function calculate(n, source, intermediate, target) {
    if (n == 1) {
        log(`Disk ${n}: ${source} -> ${target}`);
        count++;
        return;
    }

    calculate(n - 1, source, target, intermediate);
    log(`Disk ${n}: ${source} -> ${target}`);
    calculate(n - 1, intermediate, source, target);
    count++;
}
```