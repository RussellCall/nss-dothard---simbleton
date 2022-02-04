# nss-dothard---simbleton
Dothard & Simbleton project

* Objective: Build software to automate data processing for D&S paper distro company.

* Software must process all companies that have active accounts for purchasing any kind of paper from D&S.
  
* Provided with a file contains an array with 15 objects in it. Each object represents one active customer. 

* It details the address, purchasing agent, and the total dollar amount of that company's last 5 orders.
  
* App must display all business names on a web page.
  
* The ".forEach()" method on an array iterates the array.  Write logic for what to do for each item in it.

* Since each object is identical in its structure (but not its state), write some automation logic with .forEach().

* Example using .forEach() to iterate an array of objects that represent art supplies:
(/exampleDatabase.js) /* 
const supplies = [
    {
        id: 1,
        price: 12.99,
        color: "Red",
        brand: "Bloomfield",
        type: "Paint"
    },
    {
        id: 2,
        price: 75.49,
        color: "Brown",
        brand: "Illinois Art",
        type: "Easel"
    },
    {
        id: 3,
        price: 19.99,
        color: "White",
        brand: "Emerson",
        type: "Oil Paint Canvas"
    }
]

export const getSupplies = () => {
    const copyOfData = supplies.map(item => ({...item}))
    return copyOfData
}
*/

(/ExampleSupplyList.js)/*
import { getSupplies } from "./database.js"
import { Supply } from "./Supply.js"

const contentTarget = document.querySelector(".supplies")

const SupplyList = () => {
    const supplyArray = getSupplies()
    contentTarget.innerHTML = "<h1>Art Supplies</h1>"

    supplyArray.forEach(
        (supplyObject) => {
            contentTarget.innerHTML += Supply(supplyObject)
        }
    );
}
*/
(/ExampleSupply.js)/*
export const Supply = ( supplyObject ) => {
    return `
        <section class="supply">
            <h2 class="supply__type">${supplyObject.type}</h2>
            <div class="supply__price">
                Price: ${supplyObject.price}
            </div>
        </section>
    `
}
*/