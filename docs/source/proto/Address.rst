Address
=======

.. code-block:: protobuf

    message Address {
        optional RussianAddress RussianAddress = 1;
        optional ForeignAddress ForeignAddress = 2;
    }

    message RussianAddress {
        optional string ZipCode = 1;    // индекс
        required string Region = 2;     // регион (код)
        optional string Territory = 3;  // район
        optional string City = 4;       // город
        optional string Locality = 5;   // населенный пункт
        optional string Street = 6;     // улица
        optional string Building = 7;   // дом
        optional string Block = 8;      // корпус
        optional string Apartment = 9;  // квартира
    }

    message ForeignAddress {
        required string Country = 1;  // страна (код)
        required string Address = 2;  // текст адреса
    }
        

Структура данных *Address* служит для представления адресов организаций. Из двух полей *RussianAddress* и *ForeignAddress* одно обязательно должно быть заполнено.