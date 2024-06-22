## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:bbeca8e76e9f0b2aabd43cf237f395c9520129003b7da34ef430d6cdfe8c024c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:7ae5410aae08dad0cb6ea3affcb914f931b352d29e605a2c1951f006612c3a2f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 MB (637277190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217aedc04a00f223ea19f90aaf491ae9259c0de8e7f6850d163e92ea80fa4f0e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 01:07:19 GMT
SHELL [cmd /S /C]
# Sat, 22 Jun 2024 01:07:19 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 01:07:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 22 Jun 2024 01:07:22 GMT
USER ContainerUser
# Sat, 22 Jun 2024 01:07:23 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 22 Jun 2024 01:07:24 GMT
ENV MONGO_VERSION=6.0.15
# Sat, 22 Jun 2024 01:07:43 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Sat, 22 Jun 2024 01:07:53 GMT
RUN mongod --version
# Sat, 22 Jun 2024 01:07:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 22 Jun 2024 01:07:55 GMT
EXPOSE 27017
# Sat, 22 Jun 2024 01:07:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187f532ba51661689c95e6d206ad52bb9da31d7ba60a2c59d47d2c02cf027bf`  
		Last Modified: Sat, 22 Jun 2024 01:08:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b929fa2fc44d560b4d273c6ae3f8dcbf2921d745fd8f058b54828766ef4b98`  
		Last Modified: Sat, 22 Jun 2024 01:08:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd35064e8de4cefb6e2718b32fbde74617abfa5f1dcbbc3bca7b4144c88070`  
		Last Modified: Sat, 22 Jun 2024 01:08:00 GMT  
		Size: 78.4 KB (78394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f60979e6391674725d1ffa14f9c56715fc5d86e359052ac0c6b8655492bddf`  
		Last Modified: Sat, 22 Jun 2024 01:08:00 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69b1ad2d2a1d33ac2df207511dcb53f7ea6eff3eed812aeb3094b4776bc0cda`  
		Last Modified: Sat, 22 Jun 2024 01:08:00 GMT  
		Size: 275.2 KB (275193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188474e44c101918ce1a6157162b44beed89c8119064b391407e9869c07f1e90`  
		Last Modified: Sat, 22 Jun 2024 01:08:00 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80a5a1a59d0c20803e34dec2c7fdcfd25de5ecd462dcaa1b09715d66acb8529`  
		Last Modified: Sat, 22 Jun 2024 01:08:39 GMT  
		Size: 516.3 MB (516321139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9aab6fafa7931dfc26851e96d9db85db2c9779ae2e11892114de86f9e5f1e`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 95.7 KB (95693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116e9ecd9a0da515cff6811c8ce5346997995a7f42efd97405195e9303821ef5`  
		Last Modified: Sat, 22 Jun 2024 01:07:59 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e748409c3d7612403cfea8e52471a68b98d9adc0d43d562a3396f323b648c3`  
		Last Modified: Sat, 22 Jun 2024 01:07:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47154eb580ffc249acad7319fc5495f97eb3e0c3a252f4cb23ab7f2d5454f776`  
		Last Modified: Sat, 22 Jun 2024 01:07:59 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:879f556cbaab2ee4775a05f767d0095bdb319f63f318573a4d015296c7f6b813
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.8 MB (671780750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fe84d508d10910cfd45a35dc71a228e9b8b71182d7c15b991b1a469c2b038d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 15 Jun 2024 00:56:57 GMT
SHELL [cmd /S /C]
# Sat, 15 Jun 2024 00:56:59 GMT
USER ContainerAdministrator
# Sat, 15 Jun 2024 00:57:02 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 15 Jun 2024 00:57:03 GMT
USER ContainerUser
# Sat, 15 Jun 2024 00:57:05 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 15 Jun 2024 00:57:05 GMT
ENV MONGO_VERSION=6.0.15
# Sat, 15 Jun 2024 00:57:38 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Sat, 15 Jun 2024 00:57:44 GMT
RUN mongod --version
# Sat, 15 Jun 2024 00:57:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 15 Jun 2024 00:57:45 GMT
EXPOSE 27017
# Sat, 15 Jun 2024 00:57:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0f317fc703df02b37e5d4d572e5fd942e5bb144a5cc10a03f7402b0894d04e`  
		Last Modified: Sat, 15 Jun 2024 00:57:52 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c050c67e03e071f3a2ef2c45bedc1c662cd41d8d6127ca1149d8bc718ae9e13`  
		Last Modified: Sat, 15 Jun 2024 00:57:52 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbc181dbc5f35be1bb080d85a4f8e4389aa021c9875ddd671bacce05b5b5983`  
		Last Modified: Sat, 15 Jun 2024 00:57:51 GMT  
		Size: 70.8 KB (70775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4247ba2c9fd2e5b7079f4edbfa4a4b0f6a79a1d3c785795d824ac2243d6825b`  
		Last Modified: Sat, 15 Jun 2024 00:57:51 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286afe81d5d3a722b48403f6eaf23c9584aac662d5918ce09eeb270ba44b8bf5`  
		Last Modified: Sat, 15 Jun 2024 00:57:51 GMT  
		Size: 275.2 KB (275157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babc637ab1152eef689e2146c9443f3233a7090363a9c1be6abaaa9607898021`  
		Last Modified: Sat, 15 Jun 2024 00:57:51 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb6516131062cb9171ecd535b4a39304f10823bb1dbb33321a2cb36a3c9cd7d`  
		Last Modified: Sat, 15 Jun 2024 00:58:29 GMT  
		Size: 516.3 MB (516321121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6da5f734ac7d90e9e47e7d560ce572ad74548c67c755c5da613bb8fc2a16fe`  
		Last Modified: Sat, 15 Jun 2024 00:57:49 GMT  
		Size: 73.3 KB (73270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a1997a1eecfbfacb09bfa2fe0e5c39f8f79a00d9c3086038b7d1faf8ec9458`  
		Last Modified: Sat, 15 Jun 2024 00:57:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082fff46911ab4e28e6b9c88cd05de1fff18d7ce041c44d0db3125d4ea98ccba`  
		Last Modified: Sat, 15 Jun 2024 00:57:49 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a9b8f3885f3962400662d18680971a67b3c689603e4391af218fe5d11d823`  
		Last Modified: Sat, 15 Jun 2024 00:57:49 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
