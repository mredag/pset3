
$color: red;
$border-color: blue;
$fontsize: 1px;

@mixin article-card($color1,$color2,$size){
    border: $size solid $color2;
        text-align: center;

        &:nth-child(odd) {
            color: $color1;
        }
        &:nth-child(even) {
            color: $color2;
        }
}

div {
    display: flex;
    flex: 1;
    flex-direction: column;
    border: 1px solid $color;
    align-items: center;
    gap: 1rem;
    padding: 1rem;

    section{
        display: flex;

    }

    h1 {
        color: green;
        text-decoration: underline;
        text-decoration-color: gray;
    }

    article {
        @include article-card($color,$border-color,$fontsize)
    }
}
modify the code about mixin by creating a module for all declared variables.
Then, create a module with a function. This function should accept a number as parameter and return the value converted into rem. 1rem is equal to 16px
This function should be applied in the main stylesheet, so that the only sizing unit is rem.

**Suggestion:**

@function rem(...
@return calc(...
}

@use "functions" as f;
...
