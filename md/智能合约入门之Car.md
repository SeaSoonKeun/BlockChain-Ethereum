智能合约入门之Car

```solidity
// SPDX-License-Identifier: MIT
pragma solidity >0.4.22;

contract Car{
    bytes32 brand;
    uint price;
    constructor (bytes32  init_Brand, uint init_Price) {
        brand = init_Brand;
        price = init_Price;
    }
    //string数据类型要求空间很大，会导致gas消耗量增加，所以采用string memory类型，或者可以使用bytes32缩小范围.提升性能
    function setBrand(bytes32  newBrand) public {
        brand = newBrand;
    }
    function getBrand() public view returns(bytes32 ) {
        return brand;
    }
    function setPrice(uint newPrice) public {
        price = newPrice;
    }
    function getPrice() public view returns(uint){
        return price;
    } 
}
```

