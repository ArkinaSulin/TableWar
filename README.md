UI
=========================

==ADMIN Page==
  The admin page would be split to left and right
  Left is QuiTTER, 
    Background is a top down view of a farmer’s field.

    Unit Library (button) 
      Clicking on the button will load a the Unit Library page
    Map Editor (button)
    New game (button)
      Clicking on the button will load the main battle page
      Load game (button, will load the selected game below)
      A selection box with all game saved, latest on top. With following titles:
        Game name, created date and last saved date 
      Note: for load game selection box, default is the top (last saved game) double 
    Double click the item in selection box will also load game.
    “Load game” will load the main battle page with saved map, units, facing and their location, any terrain item and location

  Right is QuiVER
    Background is a view of star field. Buttons and selection box listed in Quitter, function the same.
    Unit Library in QuiVER is called Ship Library

==Unit Library page==
  Titled bar: Unit Library
  LEFT panel display all created units load from database
    On top of the LEFT panel is Filter bar
      All, Inf, Mounted, Ranged (includes siege engines), Heros (PC/NPC/Monster), Terrain (Woods, cliff <= move to map editer)

  Then images of all created units
    vercel data base: Unit_library db:
      Name: a readable name
      Alias Name: default the same as Name, for use in scenario
      Type: Inf, Archer, Calvary, Hero
      Move: Movement in ' x 5 / 50'
      TroopCount: Starting # of soldiers in the unit
      TroopHD: soldier HD, x2 if D10 or over
      UnitHD: TroopCount x TroopHD
      Morale: morale level 1-6, higher less likely to rout. 0 means will fight to last troop.
      1stCheck: calculated from Morale, amount of damage to force a morale chaeck
      2ndCheck: calculated from Morale, amount of damage to force a morale chaeck at disadvantage
      AC: Amor class acoording to D&D
      Attack: Attack Bonus acoording to D&D
      Dmg: in term of Rolls, most weapons 1x Roll, weapon damage D10+ 2 Rolls, multiply by # of attacks the troop can make.
      Special (array): ie, Shield=>shieldwall, Archer=>Aimed Shot, Calvary=>Charge, Polearm=>Phalanx ...
      MaxKill: hero ONLY, cannot kill more than he can swing.
      Images (array; formation, icon): what to display on token. may have custom images or point to default set determined by type. May be the most exiting part of the whole process.
  Interaction: clicking on the icon will bring details tothe CENTER (main) panel.

  CENTER (main) panel:
      Display a form, populating all editable attributes
        Name: a readable name
        Alias Name (hidden, only editable in scenario): default the same as Name, for use in scenario
        Type: Inf, Archer, Calvary, Hero
        Move: Movement in ' x 5 / 50'
        TroopCount: Starting # of soldiers in the unit
        TroopHD: soldier HD, x2 if D10 or over
        UnitHD: TroopCount x TroopHD
        Morale: morale level 1-6, higher less likely to rout. 0 means will fight to last troop.
        1stCheck: calculated from Morale, amount of damage to force a morale chaeck
        2ndCheck: calculated from Morale, amount of damage to force a morale chaeck at disadvantage
        AC: Amor class acoording to D&D
        Attack: Attack Bonus acoording to D&D
        Dmg: in term of Rolls, most weapons 1x Roll, weapon damage D10+ 2 Rolls, multiply by # of attacks the troop can make.
        Special (array): ie, Shield=>shieldwall, Archer=>Aimed Shot, Calvary=>Charge, Polearm=>Phalanx ...
        MaxKill: hero ONLY, cannot kill more than he can swing.
        Images (array): what to display on token. may have custom images or point to default set determined by type. May be the most exiting part of the whole process.

NOTE:   potencially an image manipulating page is required, to splice image dividing single Hero/Monster image to multiple to fit in morale and icon slot.
  


  ==Ship Library page==
  Titled bar: Shipyard
  On left is panel with all created units

  On top of the panel is Filter bar
  All, Inf, Mounted, Ranged (includes siege engines), Heros (PC/NPC/Monster), Terrain (Woods, cliff,  
