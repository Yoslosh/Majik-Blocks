# Boundary Test Data

## This is not actual test data, rather desired results for tests.

## Logic Point A: Player Health

| Boundary Input | Why It’s a Boundary | Test Data | Expected Outcome |
| :---- | :---- | :---- | :---- |
| 0 Health | Lowest Point of Health that Triggers Death | 0.00 | Death, equals 0 |
| Below 0 Health | Below Death Point | \-1.00 | Death, Negatives below 0 |
| Below 0 (Float) | Below Death Point (F) | \-0.20 | Death, Negatives below 0 |
| Above 0 (Float) | Above Death Point (F) | 0.20 | Regen after time, above 0 |
| Above 0 Health | Above Death Point | 1.00 | Regen after time, above 0 |
| 100 Health | Start Health & Max that can be Regened | 100.00 | Normal, no regen or drain |
| Below 100 Health | Below Max regen | 99.00 | Regen after time, below 100 |
| Below 100 (Float) | Below Max regen (F) | 99.80 | Regen after time, below 100 |
| Above 100 (Float) | Above Max regen (F) | 100.20 | Drain after time, above 100 |
| Above 100 Health | Above Max regen | 101.00 | Drain after time, above 100 |
| 150 Health | Maximum OverHealth | 150.00 | Drain after time, above 100 |
| Below 150 Health | Below Max Over | 149.00 | Drain after time, above 100 |
| Below 150 (Float) | Below Max Over (F) | 149.80 | Drain after time, above 100 |
| Above 150 (Float) | Above Max Over (F) | 150.20 | Drain Immediate, Above 150, set to 150 |
| Above 150 Health | Above Max Over | 151.00 | Drain Immediate, Above 150, set to 150 |

## Logic Point B: Player Damage taken

| Boundary Input | Why It’s a Boundary | Test Data | Expected Outcome |
| :---- | :---- | :---- | :---- |
| Below 1 (Negative) | Below 0, Below Mini | \-1.00 | Deal 1.00 Damage |
| Below 1 (Float) | Below Minimum | 0.01 | Deal 1.00 Damage |
| At 1 | At Minimum | 1.00 | Deal 1.00 Damage |
| Above 1 (Float) | Above Minimum | 1.01 | Deal 1.01 Damage |

## Logic Point C: Player Location & velocity

| Boundary Input | Why It’s a Boundary | Test Data | Expected Outcome |
| :---- | :---- | :---- | :---- |
| Terminal Fall Velocity | Maximum Fall Velocity | \-9.80 y units/s | Player Keeps Falling but fall Velocity stops increasing |
| Fall off floor | Minimum Fall Velocity | 0.00 y units/s | Player Fall and Fall Velocity increases |
| Jump or vertical Movement | Above Minimum | \+2.89 y units/s | Player Jumps, Fall Velocity subtracts to act as Gravity |

