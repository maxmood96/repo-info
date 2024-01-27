## `notary:server`

```console
$ docker pull notary@sha256:a6cd6cbb7664bc4625c6cddaa7b89bf36b7ec973b98b5daec4a5ccbd0d3318ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:8134a2b81f5435712d42c03a0c89be9b3488f0aab8f8aea873a6a32207611a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe921e557bd07eb7f16066fbeea3b53cbe3d0e5b8b9f9ca0f69c26de1e7c81af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9849cb67c623689dee6428eb495d4d78fc494adeb3aa721b477f41fe7da32e9`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a546db4afd50c2c679a641fc899520a00e8a4c1624ce73cc91560cc3eaf30525`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf51ddd410096a25059babc9f9281eac231a5ab07d18c15b38310478c0c28c7`  
		Last Modified: Sat, 27 Jan 2024 00:53:11 GMT  
		Size: 5.1 MB (5147836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb8803137fe5d50813360eb713146e551919ea71a0cfcc89cff69fc5c8394b1`  
		Last Modified: Sat, 27 Jan 2024 00:53:11 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54167849b92c67b574c8fb9d618b02278bf8498df1d4140c28e671cc8c3214c0`  
		Last Modified: Sat, 27 Jan 2024 00:53:11 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:1c8614c6305a939bb7cdbd579fd24bc8a173a75c09f8d1e3d8626fa66b5b37f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 KB (110720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed0121898e43c6b1fcb79b1280db42927ebde01f525d7668ecbe6a32d7a1e65`

```dockerfile
```

-	Layers:
	-	`sha256:7b1abbe7aff5aa762d66da9fe517ef451452a14107e2151e36aa39af624b7a9d`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 91.5 KB (91491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8cb2b1bdaf1d284eec8d82b2321159cf17821fb57a9ab66f62714f348728c2`  
		Last Modified: Sat, 27 Jan 2024 00:53:10 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:9f245d4b08cfa9f6934e315f60699db5caacbf638d012c4c6f16dfa10066ae4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1921e9cff1b4a1e2f42a76d36cba332469c640e928fdd53a1f88c2aa9feb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:b76d44755a1732ac572a54d4df4cfff9671b9466b719f4c80a81fd9397dbc3dc`  
		Last Modified: Thu, 30 Nov 2023 22:50:02 GMT  
		Size: 2.6 MB (2615844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f45e9feb3ba2edfc080d49db4581485558c6233268178d4453fe2a8325279b`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954094d4258a2c95977f780bff4e8892d99f25ce049f6a44b07e674e102c6b5a`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be483442a177ddfc2b11ddd623f549cd5354794cd0ff706dd6d0bf64e40286`  
		Last Modified: Fri, 01 Dec 2023 12:31:23 GMT  
		Size: 4.9 MB (4893562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e05adab9286a8bb4aff1c122c42d0226ea9168665ea394ec523ab969750dddb`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b8755f11a0174dd0e29522350fc4f07395492e9ff4f68f1014eb39dba21d0c`  
		Last Modified: Fri, 01 Dec 2023 12:31:22 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7cb971c2293a1784f771970101a6f7a684bee811b6ebd0cd9587fecf90d7ee8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc14489579644017e133610d708329c8a8152803fa0f3128d71e0e86516f3aab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fbdd79b03ed02bcc1ee5bd436fc5eed1a8d0f9978927bd06b998d1871fac80`  
		Last Modified: Fri, 01 Dec 2023 13:23:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b7089d97bf941cc859a6fba1f659eb61fe16fdcf195609d36c198237bbac30`  
		Last Modified: Fri, 01 Dec 2023 13:23:09 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385242265777aee53cdb9cd1596c53f66120c6c37db26383f77a94273e89a55c`  
		Last Modified: Fri, 01 Dec 2023 13:23:09 GMT  
		Size: 4.7 MB (4734434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a27d12e6e36e2d73a863aeeda30b5d4aec32546e67a47461df3c794ab00b55`  
		Last Modified: Fri, 01 Dec 2023 13:23:10 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382dbc1a891035042059a47d149679397bcc592ac86eca0fcfdfa5d6d07e337c`  
		Last Modified: Fri, 01 Dec 2023 13:23:10 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:c854751d0900f72cc6aaa35d5219de9528cc80a236cac79febb9c6a8bcd451de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 KB (110701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf90d60835a8fc3ef14033d00743d6c8d85e0c66003d73f41e2aa8c4854cae7d`

```dockerfile
```

-	Layers:
	-	`sha256:c68390efdef9865729ad6454da6c994b3e498e1531913754f278b153ff998ac2`  
		Last Modified: Fri, 01 Dec 2023 13:23:09 GMT  
		Size: 91.5 KB (91465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87109c58a85c344525efe08997c13854653d596b95190901d9e5d0057d845356`  
		Last Modified: Fri, 01 Dec 2023 13:23:09 GMT  
		Size: 19.2 KB (19236 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:9aa1e6871cff970fd8fb4e4bc8832346bb39f3fbba6176bee26f0875f30cca72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6ab1a3533666ecbf2c17d76fd1d8953a49bab6ee6c28b1d10a71fbe9ee11b5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:d774e70db794cae73351fd822d82d497ead52871ac6abc00892b9d5df8d14ee9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:f7286662823688d15d8d154fce6a97114514723ec2d9806a9527337308bd4dd9`  
		Last Modified: Sat, 27 Jan 2024 00:39:18 GMT  
		Size: 2.8 MB (2811055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e386d474a1d68729b72256c4f3b7073bf14717367cbd7e15ebd7e3eb149e7`  
		Last Modified: Sat, 27 Jan 2024 01:54:07 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c47c272cf9ed8f0f5786d6ec5ada36b13ec3d22f9277eb6d3d865e2825d60f8`  
		Last Modified: Sat, 27 Jan 2024 01:54:07 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6375c8e3b87b0dac0b1678f5eb28aae8bad1b52089b1ec75161ae06c806c7`  
		Last Modified: Sat, 27 Jan 2024 01:54:07 GMT  
		Size: 5.0 MB (4950790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835fa5cc15fce9cb11a457a44035d005059e373084e07321d561b621bf2f468a`  
		Last Modified: Sat, 27 Jan 2024 01:54:08 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7997662c5bc822b7de80d3bd2a38ec14e77929c62490b4d64e011c03cfa3922f`  
		Last Modified: Sat, 27 Jan 2024 01:54:08 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:3bd10a9077926e5dee0229649d7d45a6c423f3549b4df96d2d137b53671f85cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 KB (110677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ef2c0be1d7568b4a8ddd146e3a4043d18f9359f757a94de32a88b935bd8319`

```dockerfile
```

-	Layers:
	-	`sha256:20bddf3e21c7b65aada5aa964e8151a9fa20fd057c94e818c5c28bc630a5f2d1`  
		Last Modified: Sat, 27 Jan 2024 01:54:07 GMT  
		Size: 91.5 KB (91476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b46f1a2d4b41f49f8fd5bb68816188e64cdb93f69a5daa76869d24c195b3a85`  
		Last Modified: Sat, 27 Jan 2024 01:54:07 GMT  
		Size: 19.2 KB (19201 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:6bcedd9081d769ae57a98cdc4f803389e74ed61dafd425e5a6ad2adc52c2af23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8441ddc070565076798febd4bdf9771c3a0ac2da3f71b3338597d2eacd22d9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3351f370bc5e3633a2723c87d25ba725aa8a0e2029de4b1debe3a2cb508bec7`  
		Last Modified: Sat, 27 Jan 2024 09:53:58 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95d84e1abad732907afb0c768124c7f5bbefa826dce27b7283f5db07b207325`  
		Last Modified: Sat, 27 Jan 2024 09:53:57 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffd19804bc063786456254e331d29d6f117f9bf88b69e48fa3b674da542d42`  
		Last Modified: Sat, 27 Jan 2024 09:53:58 GMT  
		Size: 4.6 MB (4639143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8441f53df40e4daf96f373625add6cd752e5fec81fa5bda81a7f3308c0d866`  
		Last Modified: Sat, 27 Jan 2024 09:53:58 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4140567b12cc39de3750ed76df2428e3b5c1c743da94c9b53b62c91a13ef091`  
		Last Modified: Sat, 27 Jan 2024 09:53:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:711228e1699006ff888e7b1c2c6852328c8c5e87e455c3f072760af3fc512e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 KB (108977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd40c1760c528511efad48ec2bbbe332dd23abcec62ced7fd6049b7a1f165c5`

```dockerfile
```

-	Layers:
	-	`sha256:b733204a1e7e25f1e51875f05eb23b24b8366c9d399620beae2d056e74c78bcb`  
		Last Modified: Sat, 27 Jan 2024 09:53:58 GMT  
		Size: 89.9 KB (89877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047d4cbf037413947063dea80e1251acc6c80f71052e98db3548111183463c86`  
		Last Modified: Sat, 27 Jan 2024 09:53:57 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:66118e7982bb814a9d939808797fc0e073194732d5bcdb0afaa98c515d17ab23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375dd24b82c69922bcaab7aedbd6c4aa53455221175e092aaa73af2229bc6f37`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/server
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:3710549eb8868990a62c8d4471b58594422f5b4b00b9f1301ab37536932fc449`  
		Last Modified: Thu, 30 Nov 2023 22:43:07 GMT  
		Size: 2.6 MB (2592110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf3051463e76e45694bdac001475d6401201e997fcc6b1064dd5714221e9522`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e2029cbe168ad538ca4f618f818e1776db4675da9dcf5cb1cafb1ae26c4c73`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386697fcd6409c5fbe81e26bbcda06c92d97ea3c6a67b361b36d903e6ef46765`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 5.0 MB (4976494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa463bb75cc612787401b3735a60f0c49ce27958de1bdb663835241ff3a3a44`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9601e931117156c90946d2ee4dcf71edebc280bb2927e29c98e360fc8f2b67`  
		Last Modified: Fri, 01 Dec 2023 11:05:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:c35c2d748647d9150a218c6f9bba1ba76b2857c71608e21de4dea7e277400a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 KB (109052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd9c541de7f41ff1349988fe6c4a04896f2fbbd710e780110c9bfb08d9d0c9c`

```dockerfile
```

-	Layers:
	-	`sha256:564eda7af0ad5159f164187d1ae3bd39c19dc74b7a48b04c99c67d2b422b5029`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 89.8 KB (89822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73fd057c7a07056164b551f7e7bf9b6a82dfd98fcf9a3d0cf56ea66dd7a88b`  
		Last Modified: Fri, 01 Dec 2023 11:05:17 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
