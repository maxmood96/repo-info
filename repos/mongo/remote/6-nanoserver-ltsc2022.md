## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:40fd09ad8ece009e4e53227bc4d85cb57cf338df22eca40812246302a8923c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:efeedf5d1e9a442de52599b29a2a8b5cba77874ffb58c5e7a06febb51f894ed1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.2 MB (637245334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbed1dac6966a83ec5ef34000f5e81a23469f0e6836494f24b000242cf757ff`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:59:54 GMT
SHELL [cmd /S /C]
# Wed, 12 Jun 2024 18:59:55 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:00:00 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 12 Jun 2024 19:00:01 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:00:02 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Wed, 12 Jun 2024 19:00:03 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 12 Jun 2024 19:00:24 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Wed, 12 Jun 2024 19:00:34 GMT
RUN mongod --version
# Wed, 12 Jun 2024 19:00:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 19:00:36 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 19:00:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10a2ec97d1d703c8620267adff685e234ebf239adccf488c209730707ab79fa`  
		Last Modified: Wed, 12 Jun 2024 19:00:46 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f55663874650eb035b85a9a73fb7b24af163ca1f466156c397ddab56ef361d6`  
		Last Modified: Wed, 12 Jun 2024 19:00:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f056b518745bc8514642f9b31de7d3e2da1b2b57ee1fe9317f3f111ae1330a3f`  
		Last Modified: Wed, 12 Jun 2024 19:00:44 GMT  
		Size: 78.3 KB (78273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718ac0526f05265e9b7eac7f8550e97a4e0c027fb6f1857df0ce49daf1897bbc`  
		Last Modified: Wed, 12 Jun 2024 19:00:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3cfa5e44c5d0c4ac8887ceeb4c27bf0ac424ef9cf4994e2742875be42c07c7`  
		Last Modified: Wed, 12 Jun 2024 19:00:44 GMT  
		Size: 267.1 KB (267051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed1dc183cae47d56a51115fcdd0c0f929e0ecb20585849317c19ba536a7ce05`  
		Last Modified: Wed, 12 Jun 2024 19:00:44 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a233040d185dd6c3996d5f43cdaff2c1d12da27a5b19856e6f528adf52376696`  
		Last Modified: Wed, 12 Jun 2024 19:01:28 GMT  
		Size: 516.3 MB (516321121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7733f6103e14cd20bde8cda75890bec127d5194e729ddabccbaa1eff69eda35`  
		Last Modified: Wed, 12 Jun 2024 19:00:42 GMT  
		Size: 82.7 KB (82679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db2d55e5bc945f2deb04c3582ef44143a0eb0a69b82349671377dc61fd4c4f`  
		Last Modified: Wed, 12 Jun 2024 19:00:42 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aa041e58a81050ea7db1aa335c2b96e068941da2dd0dc076f74318f99feb77`  
		Last Modified: Wed, 12 Jun 2024 19:00:42 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df0d322c8f1f08aacd434ea388e7ae2f1c94833157dc2c78507ad46dbd076c8`  
		Last Modified: Wed, 12 Jun 2024 19:00:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
