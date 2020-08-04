## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:63a7cd9702d8b4d949af8b4ca385e040ddaacf696638f94a65ebf8473cb2ac76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:418268f504987fb4983bfd6b7fb437004ace8ac694184aac6454a5c2ecc01409
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45366923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dfb51832baf1690bcf80074f89be5bd1f12d478992d45cba265a104b7a3598`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:44:01 GMT
ADD file:342b7be45fa3887679eff01d27d004693da8196f3357b981c4ba22a87768c678 in / 
# Tue, 04 Aug 2020 15:44:01 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 15:44:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5cb330a493bb429e9ffddac9728eb9febbace7763644c25032f1ea909b193662`  
		Last Modified: Tue, 04 Aug 2020 15:50:38 GMT  
		Size: 45.4 MB (45366696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f4a86b3d28ddc46122678c427b298a61ab2906e3497419226250d9530f50d0`  
		Last Modified: Tue, 04 Aug 2020 15:50:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:165eef8acf85a4e27ebf56aca5dc5acf863fbacf59816c52429ca280ea919d15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44081376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2143fde75006c25b60dc62bf8fd4389b61d410d12c6121526b85f44ef9f44a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:17:19 GMT
ADD file:9849c3d9bfc94351af6af8b09ae67ac5c436d2adf5dc6a4466c17343f41b46be in / 
# Tue, 04 Aug 2020 03:17:26 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:18:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6ee45b7007ef9a3afb582a3b04f9b23dff044c2db3229e4d6c134638079530b2`  
		Last Modified: Tue, 04 Aug 2020 03:36:11 GMT  
		Size: 44.1 MB (44081147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44d3d05692d40f95a122965f424c46f68109d188a09b4979b559cd4fbefe37d`  
		Last Modified: Tue, 04 Aug 2020 03:36:22 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3176772e56badddf14a6836b532781f6dad4bb74101d85ba4677477de2b0ddb4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42111604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa98b3356481faa40d82f1b03b69965193d017b93b76d6c41feaa664865e7796`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:58:41 GMT
ADD file:973064f11e1c0d3ae50f3b98d16cea6d6272ab397d8c28774591385cdb572807 in / 
# Tue, 04 Aug 2020 04:58:43 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 04:58:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8cde8f65cce9352b3708283bd7d73ba6a2e2ecf103d7db2a7c34163e1293e7df`  
		Last Modified: Tue, 04 Aug 2020 05:06:54 GMT  
		Size: 42.1 MB (42111377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e60422413cc63a46f477ba19db238675c40c8767248a5d95484d1b354000938`  
		Last Modified: Tue, 04 Aug 2020 05:07:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:41aeb07692d587e4294b4f4e692ce6a6013da2ac43b41ae78ebdebf381042d34
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43171848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77a9ce16423d3cef1ddf8c46e13dc2209a97a8b6577bff75da262d3a57c726a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:46 GMT
ADD file:558ea17b7b8e667f4587a3e5510c3a2a2fc4b6503ff6075ea42440dcf274f614 in / 
# Tue, 04 Aug 2020 06:57:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:57:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e244afce4ba06049bd433e68870bf9aeac1fdcef935de1e190144ee87301f43c`  
		Last Modified: Tue, 04 Aug 2020 07:04:22 GMT  
		Size: 43.2 MB (43171620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc7da93dbc33b9496c339e91e2d70041fb11c514a7adaf8173869d187851bc8`  
		Last Modified: Tue, 04 Aug 2020 07:04:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:6728c991710bb4a5694fdd298986312bf076bdd63b4efdceac84098794b2f5e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46086969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab71c8ad02da7f5ec981d5e89696ffd86c32df1cc1db876651783d23e0225184`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:38:37 GMT
ADD file:87fb04cc1d57075d6bb55169ae9a73688c99a88e3b176d4a0d329cb0e0bc678a in / 
# Tue, 04 Aug 2020 03:38:38 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:38:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d70c3df3aa8d2a0cfe6590fa8261e03e8344be0b3d98c50a961f639b3305fc66`  
		Last Modified: Tue, 04 Aug 2020 03:43:45 GMT  
		Size: 46.1 MB (46086744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da598e44326b4ce9ca098c87586feede376484d15abaa109dad6cdebd1943f3`  
		Last Modified: Tue, 04 Aug 2020 03:43:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
