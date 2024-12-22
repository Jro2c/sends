CREATE TABLE IF NOT EXISTS `user_accounts` (
  `unique_id` varchar(36) NOT NULL, 
  `name` varchar(255) NOT NULL, 
  `rank` varchar(255) NOT NULL DEFAULT 'civ', 
  `vip` tinyint(1) NOT NULL DEFAULT 0, 
  `priority` int(11) NOT NULL DEFAULT 0, 
  `character_slots` int(11) NOT NULL DEFAULT 2, 
  `license` varchar(255) NOT NULL, 
  `discord` varchar(255), 
  `tokens` json NOT NULL, 
  `ip` INT UNSIGNED NOT NULL, 
  -- Store IPv4 as integer
  `banned` tinyint(1) DEFAULT 0, 
  `banned_by` varchar(255) NOT NULL DEFAULT 'auto_ban', 
  `reason` text DEFAULT NULL, 
  `created` timestamp NOT NULL DEFAULT current_timestamp(), 
  PRIMARY KEY (`unique_id`), 
  KEY (`license`)
) ENGINE = InnoDB DEFAULT CHARSET = utf8mb4 COLLATE utf8mb4_unicode_ci;
