# GitOps

CREATE TABLE `users_roles_mapping` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `shared_user_id` int(11) DEFAULT NULL,
  `user_id` int(11) DEFAULT NULL,
  `role_id` int(11) NOT NULL,
  `identifier` char(36) NOT NULL DEFAULT uuid(),
  PRIMARY KEY (`id`),
  UNIQUE KEY `users_roles_mapping_unique` (`identifier`),
  UNIQUE KEY `unique_parent_child` (`shared_user_id`,`user_id`)
)
