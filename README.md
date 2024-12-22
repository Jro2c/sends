CREATE TABLE IF NOT EXISTS `aty_hourly_gift` (
  `identifier` varchar(255) DEFAULT NULL,
  `hours` int(11) DEFAULT 0,
  `reward` int(11) DEFAULT 0,
  UNIQUE KEY `owner` (`identifier`) USING BTREE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;


CREATE TABLE IF NOT EXISTS `aty_hourly_tebex` (
  `transactionId` varchar(50) NOT NULL,
  `package` longtext NOT NULL,
  `redeemed` int(11) NOT NULL DEFAULT 0,
  PRIMARY KEY (`transactionId`) USING BTREE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb3 COLLATE=utf8mb3_general_ci;
