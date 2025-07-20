
![Logo](https://ps.w.org/software-license-manager/assets/banner-772x250.jpg?rev=1135848)


# Software-License-Manager

This is a code to works with Software License Manager Plugin for WordPress. The License Manager plugin gives developers the ability to control the activation and usage of a piece of software via the creation and management of licenses. By incorporating the License Manager functionality into your software, you will be able to prevent unauthorized usage of your software. This code was developed by Javier Lopez


## Features

- API Version: 1.0.0.1
- Date developed: 07/19/2025
- Labview Version: 21.0.1f6 of 32-bits ar greater
- Plugins Software License Version: 4.5.8


## Documentation

[Software License Manager page](https://wordpress.org/plugins/software-license-manager/)

## API Reference

#### Board items
![Board API](https://github.com/Javixl1/Software-License-Manager/blob/main/Image/Board%20packages.png?raw=true)

```http
  Motherboard.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `Product_Ref` | `string`    | Product reference **Suffix**                            |
| `Boad out`    | `Reference` | It can be connect to other same VIs or property node|

```http
 Read Host Name.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `Board In`    | `Reference` | Product reference input                             |
| `Boad out`    | `Reference` | It can be connect to other same VIs or property node|
| `Host Name`   | `string`    | String value where you get the **Host Name** value      |

```http
 Read OS Name.vi
```

| Parameter     | Type        | Description                                             |
| :------------ | :-------    | :--------------------------------------------------     |
| `Board In`    | `Reference`    | Product reference input                              |
| `Boad out`    | `Reference` | It can be connect to other same VIs or property node    |
| `Host Name`   | `string`    | String value where you get the **OS Name** value|

```http
 Read Owner.vi
```

| Parameter     | Type        | Description                                             |
| :------------ | :-------    | :--------------------------------------------------     |
| `Board In`    | `Reference`    | Product reference input                              |
| `Boad out`    | `Reference` | It can be connect to other same VIs or property node    |
| `Host Name`   | `string`    | String value where you get the **Owner Name** value     |

```http
 Read Product_ID.vi
```

| Parameter     | Type        | Description                                             |
| :------------ | :-------    | :--------------------------------------------------     |
| `Board In`    | `Reference`    | Product reference input                              |
| `Boad out`    | `Reference` | It can be connect to other same VIs or property node    |
| `Host Name`   | `string`    | String value where you get the **Product_ID** value     |

## API Reference

#### License items
![License API](https://github.com/Javixl1/Software-License-Manager/blob/main/Image/License%20Packages.png?raw=true)

```http
  Setting.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in` | `Reference`    | Use the object.lvclass constant         |
| `Secret Key for License Creation` | `string`    | Secrect key to creation of a new license         |
| `Secret Key for License Verif Requests`    | `string` | Secrect key to do requests fron the host device **Requested**|
| `Website`    | `Reference` | It is the webside where is located or installed the plugin, Need add https:// **Requested**|
| `Product_Ref`    | `Reference` | It can be connect to other same VIs or property node|
| `License out`    | `Reference` | It can be connect to other same VIs or property node|

```http
  Activate.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in`  | `Reference` | Use the reference object.lvclass                    |
| `ok?`         | `Boolean`   | If the action was executed led should be green      |

```http
  Deactivate.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in`  | `Reference` | Use the reference object.lvclass                    |
| `ok?`         | `Boolean`   | If the action was executed led should be green      |

```http
  Create.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in` | `Reference`    | Use the object.lvclass constant         |
| `Company Info` | `Cluster of string`    | Info that you need to complete to send to server **Requered**         |
| `ok?`         | `Boolean`   | If the action was executed led should be green      |
| `Year of License`         | `Numeric`   | Time that of duration of license      |

```http
  Check.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in` | `Reference`    | Use the object.lvclass constant         |
| `ok?`         | `Boolean`   | If the action was executed led should be green      |
| `Body`         | `String`   | Return a json format about the license status      |

```http
  Result.vi
```

| Parameter     | Type        | Description                                         |
| :------------ | :-------    | :-------------------------------------------------- |
| `License in` | `Reference`    | Use the object.lvclass constant         |
| `ok?`         | `Boolean`   | If the result was success then led indicator can be green      |
| `Body`         | `String`   | Return a json format about the license status      |


#### Example Code
![Typical activation code](https://github.com/Javixl1/Software-License-Manager/blob/main/Image/Typical%20license%20creation%20code%20.png?raw=true)

```http
  Create a request license
```

The code showed is a example where it request a license creation from you host computer to the senver in to wordpress plugin. If it is done you can se the indormation requested like next picture.

![Software-License-Manager-Plugin](https://github.com/Javixl1/Software-License-Manager/blob/main/Image/License%20on%20wordpress.png?raw=true)

## Wordpress plugin

- [Main plugin Page](https://es.wordpress.org/plugins/software-license-manager/)

## Authors

- [@javixl1](https://www.linkedin.com/in/javixl1/)

