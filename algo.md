ALGORITHM checkpoint
VAR
    ch:STRING;
    i,j,nbv,nbs,logch:INTEGER;
    const voy :="aeyiuoAEYIUO";

BEGIN
    write("donner ch");
    read (ch);
    nbv=0
    nbs=0
    FOR i FROM 0 TO long(ch) STEP 1  DO
        FOR j FROM 0 TO long(ch) STEP 1 DO
            IF (voy[j]=ch[i]) THEN
                nbv=nbv+1
            END_IF
        END_FOR
        IF (ch[i]=" ") THEN
            nbs=nbs+1
        END_IF
    END_FOR
    write(nbv,nbs,logch);
END