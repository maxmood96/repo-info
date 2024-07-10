## `nats:latest`

```console
$ docker pull nats@sha256:2773e026aef92c1d9d5a029026628c2ef6bc7415e1f998832d2d72750c8ac4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6054; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:3dcaf2dd505a30f847f629b65dab5dafe3cc7a323df700ed335e2c8ad5ae4aae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5691706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037648b294ef8e859e0b493e22af98eb82e1f4c43840f519c43a2ef77178445d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:d9553f2586d3cf48125ed778e524826c16883837cdbf976c5620e64e6c721909 in /nats-server 
# Fri, 28 Jun 2024 00:21:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:21:19 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:21:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:21:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9427b597a859edd8cf6c3f9db912cf1971aad95b44789e53abb7e5fa4fb658b`  
		Last Modified: Fri, 28 Jun 2024 00:22:09 GMT  
		Size: 5.7 MB (5691198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58462fdd375ce0f53ff471ac5bc18b4935b2a2d4b9396b6fcb9a725c2ad396d`  
		Last Modified: Fri, 28 Jun 2024 00:22:08 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8aa99ee121d03608f6faece2e30b1601b72746ced33a6c869184289c59f786a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6c8c201313d84603c1ce35c1e96a2ce180467443a8298e3db3db615e55f25c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 28 Jun 2024 00:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:a61d114683016c65f5abb4aceb60c433ed369f64521c5be50db05adb1ed41e51 in /nats-server 
# Fri, 28 Jun 2024 00:49:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:49:30 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:49:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:49:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95157ffe699fd12953d5fd0cd012dbd8b5ad27bfa28ec4b2e67d84b88eafd0a9`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 5.4 MB (5364189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874916663243269e03e7ec28639ad69e910e628f51c629bcaf16224f48e59458`  
		Last Modified: Fri, 28 Jun 2024 00:50:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:75915745bc6861eaa8fe8c92b032e8c951fa8193c064c6b3c5dbf471ea43c6a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22c1a85f90b05c7e4c410a887b1ad777431829bcb844ccd6602d3c5e039b7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:66fcced04f7fc2872c5fe1cb402802e97d1aa9c873683448584126c8104908c1 in /nats-server 
# Thu, 27 Jun 2024 23:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 27 Jun 2024 23:57:49 GMT
EXPOSE 4222 6222 8222
# Thu, 27 Jun 2024 23:57:49 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 27 Jun 2024 23:57:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4303bac97348625e176d7d570752bcf79118c8c36661a5d2b7a0adb7c36731ae`  
		Last Modified: Thu, 27 Jun 2024 23:59:29 GMT  
		Size: 5.4 MB (5355246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101bce609121fda658031401db364b878a0d8ab3cb2fd007cc6d3773d32c7593`  
		Last Modified: Thu, 27 Jun 2024 23:59:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8f223db7eb0c58c580e6357888cb69908ef1e0723c6d2427ee170fd53cf951b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbfe2d4f61aa976008acd72f6dfdc79624576981c3073c2ac2e1cb503850c0f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:94e882a0d5477010422d06722538671677be17e1303aeb2f3b515ad173708eff in /nats-server 
# Fri, 28 Jun 2024 00:40:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:40:55 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:40:56 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:40:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53bac24e35ea7041c0acb672fe34dc5774b11c9452fbce279e1539bd0aea9dde`  
		Last Modified: Fri, 28 Jun 2024 00:41:39 GMT  
		Size: 5.3 MB (5252070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388499eaad2fbd422e6427d9bbeba156ee0c65be4aed6a44f76b1ccb5cd1f06`  
		Last Modified: Fri, 28 Jun 2024 00:41:38 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:384ff223d1d9aee8f08f0972802fc3de8493205ef4d5e232f982da00fdf66a84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c9baa3eb7da42164403dcdd39c1a75fd7a40df54f2fcaa8928ebc316d6c94c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:17:04 GMT
COPY file:654abb8f8ba64bb5336fa139d9025643bf225a7221aefb482b25e81ec59c439c in /nats-server 
# Fri, 28 Jun 2024 00:17:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:17:05 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:17:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:17:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:40d3ed7debb3c5c581999695d8cac1474579d8729b2d80409a0a21af59139d51`  
		Last Modified: Fri, 28 Jun 2024 00:17:44 GMT  
		Size: 5.2 MB (5232498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108181a0cd8042df8cf1628fc15684889bf783ce54486e3ef4513ac33073a838`  
		Last Modified: Fri, 28 Jun 2024 00:17:43 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:b4f73b116646ed5a4ec2090d26b0b7568a30bad6cb030ac2613a87954dee4d07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28f491fdf4c9701a516371f0156ddbb8c521d629c4212bb10d72b309377ec72`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:3d83c0765bf0592759cb852e5833ba3e8b8f1a4b0cceb3dfc3218bc9b018246c in /nats-server 
# Fri, 28 Jun 2024 00:43:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 28 Jun 2024 00:43:06 GMT
EXPOSE 4222 6222 8222
# Fri, 28 Jun 2024 00:43:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 28 Jun 2024 00:43:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1babe0c49ee24be2fc35a0932277455e3864425e143a090c7c10ad1bf7106775`  
		Last Modified: Fri, 28 Jun 2024 00:43:59 GMT  
		Size: 5.6 MB (5554144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce9ed362ecd8bcd502652a2fe9d53863341fd71797b9920da5da89bf3595ee2`  
		Last Modified: Fri, 28 Jun 2024 00:43:58 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.6054; amd64

```console
$ docker pull nats@sha256:58a031b71d94035b7ffcac75a55d4af99f3a7324305a08175145c444335d661b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160892303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0889744b15069353592cc77e8c6750a609e1b647625d4d383ee67429dec660e8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 17:47:30 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 Jul 2024 17:47:31 GMT
RUN cmd /S /C #(nop) COPY file:597b8acb27656d6ed03f368919febfb8bdb37af32d76fdf02bde1220f352c5d1 in C:\nats-server.exe 
# Wed, 10 Jul 2024 17:47:32 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 10 Jul 2024 17:47:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 10 Jul 2024 17:47:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 10 Jul 2024 17:47:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6571be65089b158d7cd7290d7161e9a7560e859fee92e155bd4b42e3c858284`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e4bc7f31f192963e8f3a3e89f1c1b64e284d889fda14143bf16c0917fe81ad`  
		Last Modified: Wed, 10 Jul 2024 17:50:51 GMT  
		Size: 5.8 MB (5804537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888df09efeb767457fa5fd838b3c10398c77249b5bffb33a78b03f4065e9e3c6`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163346c492a1f4532039ea7cbae77aecd4a82d52f642e642dff207419ff822b8`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e15cbe5192fae81182ae87fcc0a1889f5144e9d77c78cb0cf1e3676490c6c7`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3895e939f54fd4486f6bbe60bcc460eed1327c2511d305a2f8622efc702fd4c1`  
		Last Modified: Wed, 10 Jul 2024 17:50:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
