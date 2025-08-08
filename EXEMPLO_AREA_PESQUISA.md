# exemplo de áreas de pesquisa

```xml
<entity>
    <field name="name" value="Nome do Pesquisador..."/>
    <field name="researchArea">
        <field name="biggestArea" value="Ciencias Exatas..."/>
        <field name="area" value="Ciencias da Computacao..."/>
    </field>
    <field name="researchArea">
        <field name="biggestArea" value="Ciencias Sociais..."/>
        <field name="area" value="Ciencias da Informacao..."/>
    </field>
</entity>
```

## Outra forma de representação

```xml
<entity>
    <field name="name" value="Nome do Pesquisador..."/>
    <field name="researchArea" value="grande area">
    <field name="researchArea" value="grande area / area">
    <field name="researchArea" value="grande area / area / subarea">
    <field name="researchArea" value="grande area / area / subarea / especialidade">
    <field name="researchArea" value="ciencias exatas e da terra / ciencias da computacao"> <!-- exemplo -->
</entity>
```



