## `nats:linux`

```console
$ docker pull nats@sha256:57ce9241a38769d07ce92160bc5c71e0cd2738963804100d549104b7aaa067d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

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

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:cdaef1917e97728209e2d31ad322ab062dd242d703a1107afb87a14f69c42224
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09a002d72561346cd80f81415b378fdb474d607e7890ee7c3842e80a6dc76d7`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:05:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:008e1f8859dbe07df9a3518ca5a4221602d13a6b648ffe9a29b2d00b629f16e0 in /nats-server 
# Thu, 20 Jun 2024 18:05:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:05:28 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:05:28 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:05:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e0e2aa814926dd6fcdc968764287dbba28f195a391d5ef6383057be5ff7f60d`  
		Last Modified: Tue, 21 May 2024 22:50:24 GMT  
		Size: 5.3 MB (5346515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a335ca1d1d74fac94ca3f1e18cacc14e4988b48dcc0bf71a6ad6b331a124dea`  
		Last Modified: Thu, 20 Jun 2024 18:06:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

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

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e5f9f78a2c4c5f0a7d38232239f5d2afaa03cf3a506155e952fc1b020ba4531b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef3ac3fddade2f62d6dcf1dc867c7dfe53c9a930e48efd12c3a431bbbddd414`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:f564da141e6306628e75d438342668cf55fdafa63094782cbe4449f5d6c98215 in /nats-server 
# Thu, 20 Jun 2024 19:07:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 19:07:41 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 19:07:41 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 19:07:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:94ec6b53e66c8fcb745c43768f785b3b4877166276394c340184cf7174eb38e5`  
		Last Modified: Tue, 21 May 2024 23:22:24 GMT  
		Size: 5.2 MB (5233363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ab7e76b355afe745179986de5020717321b38dae61b2b1bcaa587c3a1d6044`  
		Last Modified: Thu, 20 Jun 2024 19:08:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

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

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:1c85d5dd96f8e24bb928941e213d64cb7f634841e04009ab1224f0efbe26b65b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4c51fa5803cfee1eaaafc771c418b91caeab0549fb33309918a892cbe39864`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:0d0169a9305ddffbf54ee7393cdb2ab8fe694a4c7952574ebaeccc212cbf834b in /nats-server 
# Thu, 20 Jun 2024 18:02:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 20 Jun 2024 18:02:16 GMT
EXPOSE 4222 6222 8222
# Thu, 20 Jun 2024 18:02:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 20 Jun 2024 18:02:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1bc7712db04e70325970d818ce3314c72e3e1a2e148f5c5a7d2378504e1a05f7`  
		Last Modified: Tue, 21 May 2024 23:22:11 GMT  
		Size: 5.5 MB (5536237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b37e5601e62dd96baed2c90e93a74897cf17cd435704ed61f758023d765100`  
		Last Modified: Thu, 20 Jun 2024 18:02:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
