---
title: Robot Cost Example
description:
position: 57
category: Robots
badge: Robots
---

## Arduino Robot Example

<display-image src="/robot/arduinorobots.jpg"></display-image>

## Components

<display-image src="/robot/RobotComponents.jpg"></display-image>

## Cost Breakdown (est 2022)

<div class="flex flex-col">
  <div class="overflow-x-auto sm:-mx-6 lg:-mx-8">
    <div class="py-2 inline-block min-w-full sm:px-6 lg:px-8">
      <div class="overflow-hidden">
        <table class="min-w-full">
          <thead class="bg-gray-800 border-b">
            <tr>
              <th scope="col" class="text-sm font-medium text-white px-6 py-4 text-left">
                Component
              </th>
              <th scope="col" class="text-sm font-medium text-white px-6 py-4 text-left">
                Cost
              </th>
              <th scope="col" class="text-sm font-medium text-white px-6 py-4 text-left">
                Example Source
              </th>
            </tr>
          </thead>
          <tbody>
            <tr class="bg-gray-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                Arduino Uno
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                $12
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                <a href="https://www.amazon.ca/CANADUINO-ATmega328P-Module-Compatible-Arduino/dp/B07ZQQLDD9/ref=sr_1_9?crid=3TB6CPU9STGFJ&keywords=arduino+uno&qid=1644862194&sprefix=arduino+uno%2Caps%2C136&sr=8-9">Example on Amazon</a>
              </td>
            </tr>
            <tr class="bg-white border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                Bluetooth Module
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                $4
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                <a href="https://www.aliexpress.com/item/32786773297.html?spm=a2g0o.9042311.0.0.">Example HC-05 Module on Aliexpress</a>
              </td>
            </tr>
            <tr class="bg-gray-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                Breadboard
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap text-center">
                $6
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                <a href="https://www.solarbotics.com/product/21025">Solarbotics</a>
              </td>
            </tr>
            <tr class="bg-gray-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                DC Motors with Wheels
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap text-center">
                $4 wheels + $7.50*4 motors = $34 (Solarbotics) or different solution $10 (AliExpress)
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                <a href="https://www.solarbotics.com/product/gmpw-deal">Solarbotics</a>
                <a href="https://www.aliexpress.com/item/32867055406.html?spm=a2g0o.productlist.0.0.13256108zJpSHi&algo_pvid=a6fd6357-2914-4483-838b-566d08d0b3f4&algo_exp_id=a6fd6357-2914-4483-838b-566d08d0b3f4-5&pdp_ext_f=%7B%22sku_id%22%3A%2265512712375%22%7D&pdp_pi=-1%3B2.18%3B-1%3B-1%40salePrice%3BCAD%3Bsearch-mainSearch">AliExpress</a>
              </td>
            </tr>
            <tr class="bg-gray-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                Motor Controller
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap text-center">
                $11
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
                <a href="https://www.solarbotics.com/product/50646">SparkFun Dual Motor Driver TB6612FNG at Solarbotics</a>
              </td>
            </tr>
            <tr class="bg-gray-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                Batteries
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap text-center">
                $30 for 2 (35C 1100 mAh Lipo Batteries). Could use other more inexpensive battery options as well.
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
              </td>
            </tr>
            <tr class="bg-indigo-100 border-b">
              <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-gray-900">
                TOTAL
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap text-center">
                ~ $50 to 100
              </td>
              <td class="text-sm text-gray-900 font-light px-6 py-4 whitespace-nowrap">
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>

Note that the above costing does not include:

- Wires
- Robot Physical body. In the example shown it is a short piece of wood, plastic sheets, and some foam border.
- Screws or nails
- IF using LiPo batteries, you will also need an appropriate charger for LiPo batteries.
- Note that a half-size breadboard is sufficient (full size is shown).

<alert type="danger">
Note that if you choose to LiPo batteries, learn how to properly care for them. I also do not allow students to develop circuits powered by LiPo batteries. They must first use a USB wired connection and then when ready I will hook up the batteries for them (do not want an accidental short circuit!).
</alert>
