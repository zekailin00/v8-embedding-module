# Instruction

`g++ -I. -Iinclude path/to/src -o obj_name -fno-rtti -lv8_monolith -lv8_libbase -lv8_libplatform -ldl -Lpath/to/lib -pthread -std=c++17 -DV8_COMPRESS_POINTERS`

Reference: `https://v8.dev/`