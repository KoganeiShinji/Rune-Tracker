<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>PoE 2 - Verisium Remnant Runes (Fubgun Strat)</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0f0f12;
            color: #e2e8f0;
            padding: 20px;
            margin: 0;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
        }
        h1 {
            color: #d4a373;
            text-align: center;
            font-size: 22px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }
        .subtitle {
            text-align: center;
            color: #a0aec0;
            font-size: 14px;
            margin-bottom: 25px;
        }
        .table-container {
            background-color: #15151a;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.6);
            overflow: hidden;
            border: 1px solid #2d2d39;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            text-align: left;
        }
        th, td {
            padding: 14px 18px;
            border-bottom: 1px solid #23232b;
        }
        th {
            background-color: #1c1c24;
            color: #d4a373;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 0.5px;
        }
        tr {
            cursor: pointer;
            transition: background-color 0.15s ease;
        }
        tr:hover {
            background-color: #1e1e26;
        }
        /* Стиль для отмеченной (взятой) руны */
        tr.checked-row {
            background-color: #1b2e1e !important;
        }
        tr.checked-row td {
            color: #a3b899;
        }
        tr.checked-row .note {
            color: #718096 !important;
        }
        .tier-SS { color: #ff3366; font-weight: bold; text-shadow: 0 0 10px rgba(255,51,102,0.3); }
        .tier-S { color: #ff9f43; font-weight: bold; }
        .tier-A { color: #ffeb3b; font-weight: bold; }
        .tier-B { color: #a29bfe; font-weight: bold; }
        .tier-C { color: #74b9ff; font-weight: bold; }
        
        .note {
            font-size: 13px;
            color: #a0aec0;
            margin-top: 4px;
            line-height: 1.4;
        }
        .checkbox-cell {
            text-align: center;
            width: 60px;
            pointer-events: none; /* Клик ловит вся строка */
        }
        input[type="checkbox"] {
            width: 18px;
            height: 18px;
            accent-color: #2ecc71;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Verisium Remnants: Приоритет Рун</h1>
    <div class="subtitle">По гайду Fubgun (Кликните в любое место строки, чтобы отметить руну)</div>

    <div class="table-container">
        <table>
            <thead>
                <tr>
                    <th class="checkbox-cell">Взята</th>
                    <th style="width: 100px;">Тир</th>
                    <th style="width: 220px;">Название руны</th>
                    <th>Стратегия и примечание</th>
                </tr>
            </thead>
            <tbody id="runeTableBody">
                <!-- SS-TIER -->
                <tr data-rune-id="opulent">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-SS">SS Tier</td>
                    <td><b>Opulent Rune</b></td>
                    <td>
                        <div class="note" style="color: #ffb3c6;"><b>Абсолютный топ.</b> Если у вас длинная цепочка из 8-9 рун в конце, и на ней есть Opulent, можно завершать крафт на этом, даже если нет рун на пролиферацию (распространение модов).</div>
                    </td>
                </tr>

                <!-- S-TIER -->
                <tr data-rune-id="power">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-S">S Tier</td>
                    <td><b>Power Rune</b></td>
                    <td><div class="note">Высший приоритет среди фиолетовых рун. Дает мощный разгон наград.</div></td>
                </tr>
                <tr data-rune-id="death">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-S">S Tier</td>
                    <td><b>Death Rune</b></td>
                    <td><div class="note">Отличная базовая пролиферация и ценность в длинных рецептах.</div></td>
                </tr>
                <tr data-rune-id="bond">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-S">S Tier</td>
                    <td><b>Bond Rune</b></td>
                    <td><div class="note">Входит в топ-3 лучших фиолетовых рун по версии Fubgun.</div></td>
                </tr>

                <!-- A-TIER -->
                <tr data-rune-id="time">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-A">A Tier</td>
                    <td><b>Time Rune</b></td>
                    <td><div class="note">Отличный выбор для средних и длинных цепочек.</div></td>
                </tr>
                <tr data-rune-id="oath">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-A">A Tier</td>
                    <td><b>Oath Rune</b></td>
                    <td><div class="note">Хороший промежуточный вариант для закрытия рецептов.</div></td>
                </tr>
                <tr data-rune-id="rebirth">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-A">A Tier</td>
                    <td><b>Rebirth Rune</b></td>
                    <td><div class="note" style="color: #ffeaa7;">Единственная синяя (Rare) руна, которая заслужила А-тир благодаря своим свойствам.</div></td>
                </tr>

                <!-- B-TIER -->
                <tr data-rune-id="other-purple">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-B">B Tier</td>
                    <td><b>Остальные Фиолетовые</b></td>
                    <td><div class="note">Не особо важны. Если у вас короткая цепочка на 3-5 рун, их всегда можно просто переролить (reroll).</div></td>
                </tr>

                <!-- C-TIER -->
                <tr data-rune-id="other-blue">
                    <td class="checkbox-cell"><input type="checkbox"></td>
                    <td class="tier-C">C Tier</td>
                    <td><b>Остальные Синие</b></td>
                    <td><div class="note">Худшие руны. Используйте только при полном отсутствии альтернатив или для закрытия неважных слотов.</div></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>

<script>
    document.addEventListener('DOMContentLoaded', () => {
        const tbody = document.getElementById('runeTableBody');
        const savedStates = JSON.parse(localStorage.getItem('poe2_fubgun_runes')) || {};
        
        // Рендерим сохраненное состояние
        tbody.querySelectorAll('tr').forEach(row => {
            const id = row.getAttribute('data-rune-id');
            const checkbox = row.querySelector('input[type="checkbox"]');
            
            if (savedStates[id]) {
                checkbox.checked = true;
                row.classList.add('checked-row');
            }
            
            // Клик в ЛЮБОЕ место строки
            row.addEventListener('click', (e) => {
                checkbox.checked = !checkbox.checked;
                
                if (checkbox.checked) {
                    row.classList.add('checked-row');
                    savedStates[id] = true;
                } else {
                    row.classList.remove('checked-row');
                    delete savedStates[id];
                }
                localStorage.setItem('poe2_fubgun_runes', JSON.stringify(savedStates));
            });
        });
    });
</script>
</body>
</html>
