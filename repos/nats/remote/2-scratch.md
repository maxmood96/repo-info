## `nats:2-scratch`

```console
$ docker pull nats@sha256:aa0adeff59d1bf05e11c2328a415d2a10a16452ff2fdca70139181aad665bd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0d7c496dd4f8512bf5c61832bc16e75d805de038fc08554f33fefbcd3907c4b2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a33d0935d56b4724ba17d1c68ebc2c6abeab51f35b5c0a9d44bb9749d251c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Sep 2020 19:24:31 GMT
COPY file:22772fe85f23ca6ef547526020b6f0c57f7bb05cf1b63d4adebc9bac5872d5ce in /nats-server 
# Fri, 04 Sep 2020 19:24:31 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 04 Sep 2020 19:24:31 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 19:24:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 04 Sep 2020 19:24:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae9aef3549a0277b3c71f27b28f1616f87abeb4dfcec5ff0f2bb2109fb259b34`  
		Last Modified: Fri, 04 Sep 2020 19:25:04 GMT  
		Size: 4.1 MB (4093066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee674f246b57d546774a96e8caa7a1528c4400b153e22ce806dc1c2cb079a2e9`  
		Last Modified: Fri, 04 Sep 2020 19:25:03 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:20ea87b418a2b1273123ddef4c91956990c5fcab0bbad71523d5b6b434be249c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3811018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0459d9344473c88c51591d37f17b57327d167b6122217d7422431b328c3a1b02`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Sep 2020 20:10:08 GMT
COPY file:3ebd94b1867641b7e927368abdd7734a27a700b6431d3d384660c98fb6f91ae9 in /nats-server 
# Fri, 04 Sep 2020 20:10:21 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 04 Sep 2020 20:10:26 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 20:10:31 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 04 Sep 2020 20:10:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9388f799ec4c0c97ac0c4f5d9d8936ef881f647ba80558b3f746eea63397a54e`  
		Last Modified: Fri, 04 Sep 2020 20:11:29 GMT  
		Size: 3.8 MB (3810540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce31c20db639568dc0ccc4e73f1bdc208376b2a5b1633adc0587d4ff8aaf0c4`  
		Last Modified: Fri, 04 Sep 2020 20:11:27 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:46cae43c1deb7bbc919efb2f3271f78e195f1eaa3f8b626376dfdb633ff3b555
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a111e279efaf7a4228a57b652684e1adf34e569fc9e077ecd7350dcb0aac50`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Sep 2020 19:51:03 GMT
COPY file:c0962878fe6b8c789e4fa27fcefd32cc868d740092dee272d993d0aac72edeca in /nats-server 
# Fri, 04 Sep 2020 19:51:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 04 Sep 2020 19:51:04 GMT
EXPOSE 4222 6222 8222
# Fri, 04 Sep 2020 19:51:05 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 04 Sep 2020 19:51:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:176dd0e74c68ca9b537d3cde057424bc8bf3cff7d363d760f1ad421beaef143f`  
		Last Modified: Fri, 04 Sep 2020 19:51:45 GMT  
		Size: 3.8 MB (3792086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b07612acf847f5e6dc42a05a50dbe09be5e7de55f6028a850048895ff39137`  
		Last Modified: Fri, 04 Sep 2020 19:51:44 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
