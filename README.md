CREATE TABLE IF NOT EXISTS `angelicxs_gangterritory` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `gang` varchar(60) DEFAULT NULL,
  `boss` varchar(60) DEFAULT NULL,
  `size` float NOT NULL DEFAULT 0,
  `value` int(11) NOT NULL DEFAULT 0,
  `locationx` float DEFAULT NULL,
  `locationy` float DEFAULT NULL,
  `locationz` float DEFAULT NULL,
  `locationw` float DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=289 DEFAULT CHARSET=latin1 ROW_FORMAT=DYNAMIC;


CREATE TABLE IF NOT EXISTS `angelicxs_gangterritorylist` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `identifier` varchar(60) DEFAULT NULL,
  `gang` varchar(60) DEFAULT NULL,
  `name` varchar(60) DEFAULT NULL,
  `boss` int(11) NOT NULL DEFAULT 0,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=289 DEFAULT CHARSET=latin1 ROW_FORMAT=DYNAMIC;


--------------------------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE IF NOT EXISTS `k5_documents` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `data` longtext,
  `ownerId` varchar(50),
  `isCopy` tinyint,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE IF NOT EXISTS `k5_document_templates` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `data` longtext,
  `job` varchar(50),
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE IF NOT EXISTS `ricky_report` (
  `id` int(11) NOT NULL DEFAULT 0,
  `identifier` longtext DEFAULT NULL,
  `reportInfo` longtext DEFAULT NULL,
  `messages` longtext DEFAULT NULL,
  `staff` longtext DEFAULT NULL,
  `closed` longtext DEFAULT NULL,
  `closedFrom` longtext DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE IF NOT EXISTS `ricky_report_annotation` (
  `identifier` varchar(150) NOT NULL DEFAULT '',
  `annotation` longtext DEFAULT NULL,
  PRIMARY KEY (`identifier`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;


CREATE TABLE IF NOT EXISTS `ricky_report_staffchat` (
  `identifier` longtext DEFAULT NULL,
  `name` longtext DEFAULT NULL,
  `type` longtext DEFAULT NULL,
  `content` longtext DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

---------------------------------------------------------------------------------------------------------------------------------------------------

CREATE TABLE IF NOT EXISTS `crafting_codes` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `code` varchar(50) DEFAULT NULL,
  `coins` int(11) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=7 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

CREATE TABLE IF NOT EXISTS `crafting_data` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `identifier` varchar(50) NOT NULL,
  `exp` int(11) NOT NULL DEFAULT 0,
  `coins` int(11) DEFAULT 0,
  `boosts` int(11) DEFAULT 0,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;


CREATE TABLE IF NOT EXISTS `aty_pausemenu` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `license` varchar(255) DEFAULT NULL,
  `tasks` longtext NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=8 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

CREATE TABLE IF NOT EXISTS `motels` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `motelId` varchar(255) DEFAULT NULL,
  `motelOwner` varchar(255) DEFAULT NULL,
  `motelName` longtext NOT NULL,
  `motelPosition` longtext DEFAULT NULL,
  `motelRooms` longtext DEFAULT NULL,
  `motelWorkers` longtext DEFAULT NULL,
  `motelPurchaseCameraCenter` longtext DEFAULT NULL,
  `motelPrice` int(11) DEFAULT NULL,
  `motelActive` int(11) DEFAULT NULL,
  `motelImage` longtext DEFAULT NULL,
  `motelComments` longtext DEFAULT NULL,
  `motelMoney` int(11) DEFAULT 0,
  `motelPayments` longtext DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8 COLLATE=UTF8_GENERAL_CI;

ALTER TABLE players
ADD in_motel longtext;


CREATE TABLE IF NOT EXISTS `job_selector` (
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `identifier` varchar(255) NOT NULL,
  `exp` int(11) NOT NULL DEFAULT 0,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=23 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

CREATE TABLE IF NOT EXISTS `job_redeems` (
  `id` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
  `code` varchar(255) NOT NULL,
  `level` int(11) NOT NULL DEFAULT 1,
  UNIQUE KEY `id` (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=7 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET NAMES utf8 */;
/*!50503 SET NAMES utf8mb4 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

CREATE TABLE IF NOT EXISTS `spy_bodycam` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `job` varchar(255) NOT NULL,
  `videolink` longtext NOT NULL,
  `street` varchar(255) NOT NULL,
  `date` varchar(255) NOT NULL,
  `playername` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=42 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

/*!40103 SET TIME_ZONE=IFNULL(@OLD_TIME_ZONE, 'system') */;
/*!40101 SET SQL_MODE=IFNULL(@OLD_SQL_MODE, '') */;
/*!40014 SET FOREIGN_KEY_CHECKS=IFNULL(@OLD_FOREIGN_KEY_CHECKS, 1) */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40111 SET SQL_NOTES=IFNULL(@OLD_SQL_NOTES, 1) */;



/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET NAMES utf8 */;
/*!50503 SET NAMES utf8mb4 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

CREATE TABLE IF NOT EXISTS `hy_cargojob` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_license` varchar(255) NOT NULL,
  `experience` int(11) NOT NULL DEFAULT 0,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=17 DEFAULT CHARSET=utf8 COLLATE=utf8_general_ci;

DELETE FROM `hy_cargojob`;

/*!40103 SET TIME_ZONE=IFNULL(@OLD_TIME_ZONE, 'system') */;
/*!40101 SET SQL_MODE=IFNULL(@OLD_SQL_MODE, '') */;
/*!40014 SET FOREIGN_KEY_CHECKS=IFNULL(@OLD_FOREIGN_KEY_CHECKS, 1) */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40111 SET SQL_NOTES=IFNULL(@OLD_SQL_NOTES, 1) */;


-----------------------------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE IF NOT EXISTS `mdt_data` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `cid` VARCHAR(20) DEFAULT NULL,
  `information` MEDIUMTEXT DEFAULT NULL,
  `tags` TEXT NOT NULL,
  `gallery` TEXT NOT NULL,
  `jobtype` VARCHAR(25) DEFAULT 'police',
  `pfp` TEXT DEFAULT NULL,
  `fingerprint` VARCHAR(50) DEFAULT NULL,
  PRIMARY KEY (`cid`),
  KEY `id` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_bulletin` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `title` TEXT NOT NULL,
  `desc` TEXT NOT NULL,
  `author` varchar(50) NOT NULL,
  `time` varchar(20)  NOT NULL,
  `jobtype` VARCHAR(25) DEFAULT 'police',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_reports` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `author` varchar(50) DEFAULT NULL,
  `title` varchar(255) DEFAULT NULL,
  `type` varchar(50) DEFAULT NULL,
  `details` LONGTEXT DEFAULT NULL,
  `tags` text DEFAULT NULL,
  `officersinvolved` text DEFAULT NULL,
  `civsinvolved` text DEFAULT NULL,
  `gallery` text DEFAULT NULL,
  `time` varchar(20) DEFAULT NULL,
  `jobtype` varchar(25) DEFAULT 'police',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_bolos` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `author` varchar(50) DEFAULT NULL,
  `title` varchar(50) DEFAULT NULL,
  `plate` varchar(50) DEFAULT NULL,
  `owner` varchar(50) DEFAULT NULL,
  `individual` varchar(50) DEFAULT NULL,
  `detail` text DEFAULT NULL,
  `tags` text DEFAULT NULL,
  `gallery` text DEFAULT NULL,
  `officersinvolved` text DEFAULT NULL,
  `time` varchar(20) DEFAULT NULL,
  `jobtype` varchar(25) NOT NULL DEFAULT 'police',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_convictions` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `cid` varchar(50) DEFAULT NULL,
  `linkedincident` int(11) NOT NULL DEFAULT 0,
  `warrant` varchar(50) DEFAULT NULL,
  `guilty` varchar(50) DEFAULT NULL,
  `processed` varchar(50) DEFAULT NULL,
  `associated` varchar(50) DEFAULT '0',
  `charges` text DEFAULT NULL,
  `fine` int(11) DEFAULT 0,
  `sentence` int(11) DEFAULT 0,
  `recfine` int(11) DEFAULT 0,
  `recsentence` int(11) DEFAULT 0,
  `time` varchar(20) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_incidents` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `author` varchar(50) NOT NULL DEFAULT '',
  `title` varchar(50) NOT NULL DEFAULT '0',
  `details` LONGTEXT NOT NULL,
  `tags` text NOT NULL,
  `officersinvolved` text NOT NULL,
  `civsinvolved` text NOT NULL,
  `evidence` text NOT NULL,
  `time` varchar(20) DEFAULT NULL,
  `jobtype` varchar(25) NOT NULL DEFAULT 'police',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_logs` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `text` text NOT NULL,
  `time` varchar(20) DEFAULT NULL,
  `jobtype` varchar(25) DEFAULT 'police',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_vehicleinfo` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `plate` varchar(50) DEFAULT NULL,
  `information` text NOT NULL DEFAULT '',
  `stolen` tinyint(1) NOT NULL DEFAULT 0,
  `code5` tinyint(1) NOT NULL DEFAULT 0,
  `image` text NOT NULL DEFAULT '',
  `points` int(11) DEFAULT 0,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_weaponinfo` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `serial` varchar(50) DEFAULT NULL,
  `owner` varchar(50) DEFAULT NULL,
  `information` text NOT NULL DEFAULT '',
  `weapClass` varchar(50) DEFAULT NULL,
  `weapModel` varchar(50) DEFAULT NULL,
  `image` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `serial` (`serial`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `mdt_impound` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `vehicleid` int(11) NOT NULL,
  `linkedreport` int(11) NOT NULL,
  `fee` int(11) DEFAULT NULL,
  `time` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;


CREATE TABLE IF NOT EXISTS `addon_account` (
  `name` varchar(60) NOT NULL,
  `label` varchar(100) NOT NULL,
  `shared` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `addon_account_data` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `account_name` varchar(100) DEFAULT NULL,
  `money` int(11) NOT NULL,
  `owner` varchar(46) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `index_addon_account_data_account_name_owner` (`account_name`,`owner`),
  KEY `index_addon_account_data_account_name` (`account_name`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `wasabi_bans` (
  `author` varchar(40) DEFAULT NULL,
  `player` varchar(40) DEFAULT NULL,
  `license` varchar(50) DEFAULT NULL,
  `ip` varchar(25) DEFAULT NULL,
  `discord` varchar(40) DEFAULT NULL,
  `reason` varchar(100) DEFAULT NULL,
  `ban_time` int(50) NOT NULL,
  `exp_time` varchar(40) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `boombox_songs` (
  `citizenid` varchar(64) NOT NULL,
  `label` varchar(30) NOT NULL,
  `link` longtext NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `sd_codes` (
  `identifier` VARCHAR(120) NOT NULL,
  `code` VARCHAR(12) NOT NULL,
  `uses` int(20) NOT NULL,
  `playtime` int(20) NOT NULL,
  `usedcodes` LONGTEXT NOT NULL,
  `usedfriendcodes` LONGTEXT NOT NULL,
  `rewardstoclaim` LONGTEXT NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `sd_codes`
  ADD PRIMARY KEY (`identifier`)
;

CREATE TABLE IF NOT EXISTS `sd_createdcodes` (
  `code` VARCHAR(60) NOT NULL,
  `reward_data` LONGTEXT NOT NULL,
  `date_creation` datetime DEFAULT NULL,
  `date_deletion` datetime DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `sd_createdcodes`
  ADD PRIMARY KEY (`code`)
;

CREATE TABLE IF NOT EXISTS `sdc_pumpkinsmash_score` (
  `ident` VARCHAR(140) NOT NULL,
  `psmashed` int(20) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `sdc_pumpkinsmash_score`
  ADD PRIMARY KEY (`ident`)
;

CREATE TABLE IF NOT EXISTS `sdc_pumpkinsmash_users` (
  `ident` VARCHAR(140) NOT NULL,
  `name` VARCHAR(40) NOT NULL,
  `tcaught` int(20) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

ALTER TABLE `sdc_pumpkinsmash_users`
  ADD PRIMARY KEY (`ident`)
;

-- Player Skills Table
CREATE TABLE IF NOT EXISTS `player_skills` (
    `citizenid` varchar(50) NOT NULL,
    `skills` json DEFAULT '{}',
    PRIMARY KEY (`citizenid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

-- Player Reputation Table
CREATE TABLE IF NOT EXISTS `player_reputation` (
    `citizenid` varchar(50) NOT NULL,
    `reputation` json DEFAULT '{}',
    PRIMARY KEY (`citizenid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

-- Player Licences Table
CREATE TABLE IF NOT EXISTS `player_licences` (
    `citizenid` varchar(50) NOT NULL,
    `licences` json DEFAULT '{}',
    PRIMARY KEY (`citizenid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `jbbvtc` (
  `citizenid` varchar(255) DEFAULT NULL,
  `total_course` int(11) NOT NULL DEFAULT 0,
  `total_earning` int(11) NOT NULL DEFAULT 0,
  `rate` double NOT NULL DEFAULT 5.0,
  `history` text DEFAULT '[]',
  PRIMARY KEY (`citizenid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `lapraces` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(50) DEFAULT NULL,
  `checkpoints` text DEFAULT NULL,
  `records` text DEFAULT NULL,
  `creator` varchar(50) DEFAULT NULL,
  `distance` int(11) DEFAULT NULL,
  `raceid` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=35 DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `farming_crops` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `owner` varchar(50) NOT NULL,
  `crop` varchar(255) NOT NULL,
  `prop` varchar(255) NOT NULL,
  `hunger` double NOT NULL,
  `thirst` double NOT NULL,
  `quality` double NOT NULL,
  `growth` double NOT NULL,
  `growthrate` int(11) NOT NULL,
  `degraderate` int(11) NOT NULL,
  `coords` text DEFAULT NULL,
  `zheight` int(11) NOT NULL,
   PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4;

CREATE TABLE IF NOT EXISTS `farming_warehouse` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `crop` varchar(255) NOT NULL,
  `amount` bigint(255) NOT NULL DEFAULT 0,
   PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4;

INSERT INTO `farming_warehouse` (`crop`) VALUES ('Barley'), ('Maize'), ('Potato'), ('Mushroom'), ('Apple'), ('Orange'), ('Lemon'), ('Lime'), ('Lettuce'), ('CactusFruit'), ('Tomato'), ('Strawberry'), ('Blueberry'), ('Milk'), ('Egg'), ('Pineapple');

-----------------------------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE IF NOT EXISTS `mdt_clocking` (
  `id` int(10) NOT NULL AUTO_INCREMENT,
  `user_id` varchar(50) NOT NULL DEFAULT '',
  `firstname` varchar(255) NOT NULL DEFAULT '',
  `lastname` varchar(255) NOT NULL DEFAULT '',
  `clock_in_time` varchar(255) NOT NULL DEFAULT '',
  `clock_out_time` varchar(50) DEFAULT NULL,
  `total_time` int(10) NOT NULL DEFAULT '0',
  PRIMARY KEY (`user_id`) USING BTREE,
  KEY `id` (`id`) USING BTREE
) ENGINE=InnoDB AUTO_INCREMENT=7 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;


DROP TABLE IF EXISTS `properties`;

CREATE TABLE IF NOT EXISTS `properties` (
    `property_id` int(11) NOT NULL AUTO_INCREMENT,
    `owner_citizenid` varchar(50) NULL,
    `street` VARCHAR(100) NULL,
    `region` VARCHAR(100) NULL,
    `description` LONGTEXT NULL,
    `has_access` JSON NULL DEFAULT (JSON_ARRAY()), -- [citizenid1, citizenid2, ...]
    `extra_imgs` JSON NULL DEFAULT (JSON_ARRAY()),
    `furnitures` JSON NULL DEFAULT (JSON_ARRAY()),
    `for_sale` boolean NOT NULL DEFAULT 1,
    `price` int(11) NOT NULL DEFAULT 0,
    `shell` varchar(50) NOT NULL,
    `apartment` varchar(50) NULL DEFAULT NULL, -- if NULL then it's a house
    `door_data` JSON NULL DEFAULT NULL, -- {"x": 0.0, "y": 0.0, "z": 0.0, "h": 0.0, "length": 0.0, "width": 0.0}
    `garage_data` JSON NULL DEFAULT NULL, -- {"x": 0.0, "y": 0.0, "z": 0.0} -- NULL if no garage
    `zone_data` JSON NULL DEFAULT NULL,
    PRIMARY KEY (`property_id`),
    CONSTRAINT `FK_owner_citizenid` FOREIGN KEY (`owner_citizenid`) REFERENCES `players` (`citizenid`) ON UPDATE CASCADE ON DELETE CASCADE,
    CONSTRAINT `UQ_owner_apartment` UNIQUE (`owner_citizenid`, `apartment`) -- A character can only own one apartment
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
-----------------------------------------------------------------------------------------------------------------------------------------------------

CREATE TABLE IF NOT EXISTS `wasabi_evidence` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `data` longtext NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8;

CREATE TABLE IF NOT EXISTS `wasabi_fingerprints` (
  `identifier` varchar(100) NOT NULL,
  PRIMARY KEY (`identifier`)
);

CREATE TABLE IF NOT EXISTS `wasabi_manual_prints` (
  `identifier` varchar(100) NOT NULL,
  `firstname` varchar(50) NOT NULL,
  `lastname` varchar(50) NOT NULL,
  PRIMARY KEY (`identifier`)
);

CREATE TABLE IF NOT EXISTS `multijobs` (
  `citizenid` varchar(100) NOT NULL,
  `jobdata` text DEFAULT NULL,
  PRIMARY KEY (`citizenid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-----------------------------------------------------------------------------------------------------------------------------------------------------

CREATE TABLE IF NOT EXISTS `players_xp` (
    `id` INT NOT NULL AUTO_INCREMENT,
    `identifier` VARCHAR(255) NOT NULL UNIQUE,
    `xp_data` LONGTEXT NOT NULL,
    PRIMARY KEY (`id`)
);

------------------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE IF NOT EXISTS `bossmenu_application` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`job` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`citizenid` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`name` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`gender` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`date` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`reason` LONGTEXT NULL DEFAULT NULL COLLATE 'utf8mb4_bin',
	INDEX `id` (`id`) USING BTREE
)COLLATE='utf8mb3_general_ci' ENGINE=InnoDB;

CREATE TABLE IF NOT EXISTS `bossmenu_bills` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`job` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`rcdate` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`untildate` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`amount` INT(11) NULL DEFAULT NULL,
	`toname` LONGTEXT NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`tocitizenid` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`fromname` LONGTEXT NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	`fromcitizenid` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8mb3_general_ci',
	INDEX `id` (`id`) USING BTREE
) COLLATE='utf8mb3_general_ci' ENGINE=InnoDB;

-----------------------------------------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE economic_system_price (
    items VARCHAR(75) PRIMARY KEY,
    label VARCHAR(75),
    category VARCHAR(75),
    salesbeforepricechange_config INT,
    maxitemspersell INT,
    maxincreaseprice INT,
    maxdecreaseprice INT,
    sales_before_price_change INT,
    price INT NOT NULL
);


CREATE TABLE economic_system_price_changes (
    items VARCHAR(75),
    price_change INT NOT NULL,
    PRIMARY KEY (items)
);


CREATE TABLE economic_system_price_history (
    item VARCHAR(75) PRIMARY KEY,
    label VARCHAR(75),
    30min INT,
    60min INT,
    4h INT,
    12h INT,
    24h INT,
    48h INT,
    72h INT
);

CREATE TABLE economic_system_price_history_log (
    item VARCHAR(75) PRIMARY KEY,
    label VARCHAR(75),
    30min INT,
    60min INT,
    4h INT,
    12h INT,
    24h INT,
    48h INT,
    72h INT
);
