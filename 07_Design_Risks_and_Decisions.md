# Design Risks and Open Decisions

| Topic | Risk / uncertainty | Required action |
|---|---|---|
| Touchscreen | Interface and power vary by model | Select exact model and read datasheet |
| Power supply | Combined peripheral load may exceed capacity | Prepare power budget |
| Battery | Unsafe or unstable power if poorly designed | Use a properly engineered protected solution |
| Cooling | Enclosure may trap heat | Plan airflow and perform thermal tests |
| NVMe | HAT, SSD, and cable compatibility vary | Verify PCIe solution and mechanical fit |
| GPIO | 5V signals can damage the Pi | Use 3.3V-compatible interfaces / level shifting |
| Enclosure | Connectors and cables need clearance | Create dimensioned mechanical layout |
| PCB | Incorrect assumptions can damage hardware | Verify schematic against official pinouts and datasheets |

## Decisions to confirm
- Exact touchscreen model
- microSD capacity and rating
- Whether NVMe is needed in the first build
- Keyboard and pointing-device form factor
- Battery runtime target, if portable battery power is required
- Enclosure dimensions and material
- Optional sensors, camera, audio, or STM32 controller
