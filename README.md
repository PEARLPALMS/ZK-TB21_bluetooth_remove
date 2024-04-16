# How to remove bluetooth from ZK-TB21 or ZK-MT21

## ZK-TB21 is 2.1ch power amplifier.<br>
<img src="./image/ZK-TB21.png" width="80%">
<br>

## ZK-MT21 is 2.1ch power amplifier.<br>
<img src="./image/ZK-MT21.png" width="80%">
<br>

## Bluetooth chip is JL AC23BP. No datasheet available.<br>
<img src="./image/AC23BP.png" width="40%">
<br>

## Remove the chip from the board.<br>
<img src="./image/remove_chip.png" width="60%">
<br>

## Removed IC.<br>
<img src="./image/AC23BP_chip.png" width="40%">
<br>

## Short the power signal.<br>
> short IC pin No 6 and C9.<br>
<table>
  <tbody>
    <tr><td>Pin 6</td><td><-- short --></td><td>C9</td></tr>
  </tbody>
</table>
* M5350B regulator is MST5350BTS. 35v to 5v.<br>

<img src="./image/short_power_signal.png" width="60%">
<br>

## Bypass audio signal.<br>
> short C2 and C15. Left audio channel signal.<br>
> short C3 and C17. Right audio channel signal.<br>
<table>
  <tbody>
    <tr><td>C2</td><td><-- short --></td><td>C15</td></tr>
    <tr><td>C3</td><td><-- short --></td><td>C17</td></tr>
  </tbody>
</table>

<img src="./image/line_in.png" width="40%"> <img src="./image/line_out.png" width="40%">
<br>

## Board with Bluetooth removed.<br>
<img src="./image/removed_bt_chip.png" width="80%">
<br>

## AC23BP chip pin layout
<table>
  <thead>
    <tr>
      <th colspan="4">AC23BP</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>unknown</td><td>24</td><td>unknown</td></tr>
    <tr><td>2</td><td>unknown</td><td>23</td><td>unknown</td></tr>
    <tr><td>3</td><td>unknown</td><td>22</td><td>unknown</td></tr>
    <tr><td>4</td><td>unknown</td><td>21</td><td>unknown</td></tr>
    <tr><td>5</td><td>unknown</td><td>20</td><td>unknown</td></tr>
    <tr><td>6</td><td>Power signal</td><td>19</td><td>unknown</td></tr>
    <tr><td>7</td><td>R signal out</td><td>18</td><td>Vcc</td></tr>
    <tr><td>8</td><td>L signal out</td><td>17</td><td>unknown</td></tr>
    <tr><td>9</td><td>unknown</td><td>16</td><td>unknown</td></tr>
    <tr><td>10</td><td>unknown</td><td>15</td><td>unknown</td></tr>
    <tr><td>11</td><td>GND</td><td>14</td><td>L signal in</td></tr>
    <tr><td>12</td><td>unknown</td><td>13</td><td>R signal in</td></tr>
  </tbody>
</table>

## Cheat sheet

> <table>
>   <tbody>
>     <tr><td>Pin 6</td><td><-- short --></td><td>Pin 18</td></tr>
>     <tr><td>Pin 7</td><td><-- short --></td><td>Pin 13</td></tr>
>     <tr><td>Pin 8</td><td><-- short --></td><td>Pin 14</td></tr>
>   </tbody>
> </table>
