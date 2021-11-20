## `nats:latest`

```console
$ docker pull nats@sha256:dba2bbbe7e9dd7c39a43a53a5d4beeaae542ee98dae82b64aed895c6589e8f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:a432c76b3a2a54bb6fb3b86e877366d6aa21583ebe4f2ac823e64c45eaa8fca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df40d7176d11e40e19fccfad2680ae991e2c854614f48d103ab2113c0bbaa764`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 22:58:51 GMT
COPY file:96d98498cda3c5da3dc5832a7d618a3bb7f4a096b3ea637e2f8cabbfb29aafda in /nats-server 
# Fri, 19 Nov 2021 22:58:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 22:58:52 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 22:58:53 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 22:58:53 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ccbcbf096ecb0f4372da6ec705628eb29f193a58043de9630df8acf8cc054adb`  
		Last Modified: Fri, 19 Nov 2021 23:01:12 GMT  
		Size: 4.2 MB (4238884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acebffb1f0ae9c7c56391d05ec7a9017310843497ef8f788ccb7fdf9487811c8`  
		Last Modified: Fri, 19 Nov 2021 23:01:09 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a2128869e3ca420fafa695c880ff2e5c081643a029a8779a6eeec898629e36d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08762624e57d46383c02de1abccfc4c29555fa4bb40f315d659a023ac90098d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:01:53 GMT
COPY file:e12b786ebded388f1ce441cbb64f5164d1e259a5f4da426728fd95521a79c6b6 in /nats-server 
# Fri, 19 Nov 2021 23:01:54 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:01:54 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:01:55 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:01:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1d5938b236103203b9eb22184fe7e2ec0ffbd51bc371b4d86b56ad8ce19084cd`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 4.2 MB (4186496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e926f0e8ecd40b008d6f98741369d8c9c17aeb7cb228b7af14e7b9424c6cc56`  
		Last Modified: Fri, 19 Nov 2021 23:03:11 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:905989f3a6b51bca9680b352fd5a4cc271c355fe1f97bc891436699220a6dc15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107424291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc5b97cb5590745b1ceee71f3fa39e6182c08aa0778a902b59edef61785e388`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 19 Nov 2021 23:16:56 GMT
RUN cmd /S /C #(nop) COPY file:cb348e461b3d96ac80f8049551e5a2f64ad993b7e0766d87ab5ab5fdd94589b6 in C:\nats-server.exe 
# Fri, 19 Nov 2021 23:16:57 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Fri, 19 Nov 2021 23:16:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:16:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 19 Nov 2021 23:17:00 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9a2a1dd5182104e73dd0b99871b9421cef25f8493a107f6c5851e604a0c805`  
		Last Modified: Fri, 19 Nov 2021 23:20:49 GMT  
		Size: 4.6 MB (4634936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea376684ddbfce1b9e46c526a7dbe800a8e6a7423d96f16cca44e1ac0610b13b`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdadde7749a61c1e452864079f7e483484220f0ae3fa7f7bd7244e01c51564e`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c305401f02bde38a326c77b9088b6a7a2a01a5babed79ec98c244a5c6006588`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4957be82dbf1c2d1fdab2d9f4604991c3bbf7c9ff6fa46efeee39dd1086ed3`  
		Last Modified: Fri, 19 Nov 2021 23:20:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
