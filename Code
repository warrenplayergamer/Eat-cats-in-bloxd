# Eat-cats-in-bloxd
You can now eat cats
code by SOMPENDER
code :
```
// WorldCode
// EatCats V1 by Sompender

SOUNDS = [["burp", .5], ["burp", .7], ["eat1", .3], ["eat1", .5]];
COOLDOWN = 2500;
onPlayerAttemptAltAction = (id, x, y, z, block, eId) => {
  if (eId && api.getEntityType(eId) === "Wildcat") {
    if (api.getEffects(id).includes("Fat")) return "preventAction";
    api.killLifeform(eId);
    for (const s of SOUNDS) api.playSound(id, s[0], 1, s[1]);
    try { api.applyHealthChange(id, 50) } catch {};
    api.applyEffect(id, "Fat", COOLDOWN, { inbuiltLevel: 1, icon: "Steak" });
    api.applyEffect(id, "Damage", 12e3, { inbuiltLevel: 2 });
  }
}
