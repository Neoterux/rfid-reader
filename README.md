# [TECH-397] RFID Reader

Proyecto de Materia Integradora que busca desarrollar una solución para el control eficiente del
stock de inventario, así también como agilizar procesos como la contabilización del stock físico
disponible.


## Capas de la Aplicación

```mermaid
block-beta
    columns 2
    ui["User Interface"]:2

    block: HARDWARE:1
        columns 1
        a["HARDWARE LAYER"]
        block:HWDESC:1
            columns 2
            rfidman["RFID Manager"]
            cex("Command Execution Layer")
            hal("RFID Abstraction and Vendor Detection")
            driver("Vendor Implementation and SDK Layer")
        end
    end

    block:INT:1
        internet("Internet Control Layer")
    end

    block:DBLOCK:2
        columns 1
        data("Data Management")
        block:RPO
            repo("Repository")
            db("Local Database")
            api("API Communication Feature")
        end
    end
```