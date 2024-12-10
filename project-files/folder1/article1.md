---
layout: default
title:  "Need for MFA"
category: "Case Study"
sub-category: "Security"
courses: [SC-200,SC-300, AZ-500]
---

<!DOCTYPE html>
<html>
<head>
    <style>
        .grid {
            display: grid;
            grid-template-columns: repeat(12, 30px); /* Adjust columns as per the crossword size */
            gap: 2px;
        }
        .cell {
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 16px;
        }
        .editable {
            border: 1px solid #000;
            background-color: #fff;
        }
        .non-editable {
            background-color: #ccc;
            border: 1px solid #ccc;
        }
        input {
            width: 100%;
            height: 100%;
            border: none;
            text-align: center;
            font-size: 16px;
        }
        input:focus {
            outline: none;
        }
    </style>
</head>
<body>

<div class="grid">
    <!-- Row 1 -->
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="Z"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="U"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="R"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="E"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 2 -->
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="C"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="O"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="M"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="O"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="D"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="B"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 3 -->
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="P"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="I"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="E"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>

    <!-- Row 4 -->
    <div class="cell non-editable"></div>
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="F"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="U"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="N"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="C"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="T"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="I"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="O"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="N"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell non-editable"></div>

    <!-- Row 5 -->
    <div class="cell non-editable"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="Z"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="U"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="R"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="E"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="Q"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="L"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="D"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="T"></div>

    <!-- Row 6 -->
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="Z"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="U"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="R"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="E"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="S"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="Q"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="L"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="D"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="T"></div>
    <div class="cell editable"><input type="text" maxlength="1" value="A"></div>
</div>

</body>
</html>
