# Instruction

`g++ -I. -Iinclude path/to/src -o obj_name -fno-rtti -lv8_monolith -lv8_libbase -lv8_libplatform -ldl -Lpath/to/lib -pthread -std=c++17 -DV8_COMPRESS_POINTERS`

Reference: `https://v8.dev/`

Static library has about 4GB. Download it from https://drive.google.com/drive/folders/1pYB72Gyvzwr98U6TKKfR3_cykg550mXm?usp=sharing