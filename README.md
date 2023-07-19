# idTip

Adds anything's IDs to the ingame tooltips.

![Screenshot](https://i.imgur.com/S6kwDlz.png)

Please report any requests/bugs through an [issue](https://github.com/ItsJustMeChris/idTip-Community-Fork/issues/new).

## Downloads

<p align="left">
<p>Mostly Up To Date</p>
    <a href="https://www.curseforge.com/wow/addons/idtip-community-fork"><img src="https://img.shields.io/badge/Download%20From-Curse-blue" alt="CurseForge" /></a>
</p>

<p align="left">
<p>Always Up To Date</p>
    <a href="https://nightly.link/ItsJustMeChris/idTip-Community-Fork/workflows/main/master/idTip.zip"><img src="https://img.shields.io/badge/Download%20-Direct From GitHub-blue" alt="idTip.zip" /></a>
</p>

## Usage

```
Hover over stuff

You can enable/disable displaying IDs with the command

/idtip
```

## API

##### IDTip now exposes a LibStub('idTip') library

```lua

-- The kinds of IDs you can apply to Tooltips
IDTip.kinds = {
  spell = "SpellID",
  itemspell = "ItemSpellID",
  item = "ItemID",
  unit = "NPC ID",
  quest = "QuestID",
  talent = "TalentID",
  achievement = "AchievementID",
  criteria = "CriteriaID",
  ability = "AbilityID",
  currency = "CurrencyID",
  artifactpower = "ArtifactPowerID",
  enchant = "EnchantID",
  bonus = "BonusID",
  gem = "GemID",
  mount = "MountID",
  companion = "CompanionID",
  macro = "MacroID",
  equipmentset = "EquipmentSetID",
  visual = "VisualID",
  source = "SourceID",
  species = "SpeciesID",
  icon = "IconID",
  areapoi = "AreaPoiID",
  vignette = "VignetteID",
  ctrait = "TraitNodeID",
  cgarrisontalent = "GarrisonTalentID",
  ccovenantsanctumtree = "SanctumTalentTreeID",
  cgarrisontalenttree = "GarrisonTalentTreeID",
  mission = "MissionID",
  guid = "GUID",
  traitconfig = "TraitConfigID",
  traitentry = "TraitEntryID",
  traitdef = "TraitDefinitionID",
  profspecnode = "ProfessionNodeID",
  rootprofspecnode = "RootProfNodeID",
  profspectreeid = "ProfessionTreeID",
  expansion = "ExpansionID",
  unittoken = "CasterToken"
}

-- Inverse of the kinds table, useful for going back and forth programmatically for whatever reason
IDTip.kinds_inverse = table_invert(IDTip.kinds)

-- Add raw text to a tooltip
-- @tooltip | Tooltip frame IE: GameTooltip
-- @line | string | number the text to apply to the tooltip
function IDTipLib:addGenericLine(tooltip, line)

-- Add a 'kinds' line to a tooltip
-- @tooltip | Tooltip frame IE: GameTooltip
-- @id | a single id (string | number) or an array of id's
-- @kind | an IDTip.kinds kind
function IDTipLib:addLine(tooltip, id, kind)

-- Programmatically get all IDTip IDs applied to a tooltip
function IDTipLib:GetAllIds()

-- Add an IDTip kinds line based on the text value of a kinds key
-- @tooltip | Tooltip frame IE: GameTooltip
-- @id | a single id (string | number) or an array of id's
-- @kind | an IDTip.kinds kind
function IDTipLib:addLineByKind(frame, id, kind)

-- Register the addon loaded event listener for a specific addon
-- @addon | string Addon name
-- @cb | function callback method to invoke when addon loaded
function IDTipLib:RegisterAddonLoad(addon, cb)

-- Log a message to the chat with IDTip 'branding'
-- @... | vararg parameters to add to the print statement
function IDTipLib:Log(...)

-- Check if a kind is enabled in the IDTIP_CONFIG
-- @kind | string or IDTip.Kinds value
function IDTipLib:kindEnabled(kind)

```

## Contributors

[hammerOwen](https://github.com/hammerOwen)

[zarillion](https://github.com/zarillion)

[Dunati](https://github.com/Dunati)

[agentschmitt](https://github.com/agentschmitt)
