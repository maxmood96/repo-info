<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:0eba6d85f86deb5371ed86229a7c5d2b46119ae55f50de1de79b936d081e3079
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
$ docker pull notary@sha256:f9e3c9ec1019bea906aa7405295ecf1381f7f6475f53590adcd15c23d1d0869e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84029b580ae55ba49fd85302ea06cb5cd4e1bed5ac274e721d0f4f0666676711`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
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
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871114d42287b33918110eb07523b39cc14160b33769f724b170bf43a4c2448`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25e6b54e0007f0999c84ca49cf883a52575b965111792bbe02d2f093c96ac81`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c11637e18c4d43df896acfb974619c241e4e37c095aeffeb276ab3a2cdf406`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 4.7 MB (4734451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f419ca26bb54623d108a021c2c2c34eaed1c16f92fa2229285b99b0282256dd`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ace66c72250b80705eea11b9c2d2f3ba3369734a40cd6cd6354470eae494b`  
		Last Modified: Sat, 27 Jan 2024 20:32:28 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:e2b01b3020019bbc8c85dae68cfeb4c58807a7ae34573688b4f46109f7402711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 KB (110568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b16dcbaac1ebcfa1229ae13647f11cfd29977ea29c5999f14fdaa29507e16a6`

```dockerfile
```

-	Layers:
	-	`sha256:8e76965d142c8d838b9c5bb1a2db25f48b35befdf374a819173f93cc04632dd0`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 91.5 KB (91498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c36adb1e2075dd8b4f29949c82350818cecaa8c296f6d8a94c58990f468575`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 19.1 KB (19070 bytes)  
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

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:0eba6d85f86deb5371ed86229a7c5d2b46119ae55f50de1de79b936d081e3079
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

### `notary:server-0.7.0` - linux; amd64

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

### `notary:server-0.7.0` - unknown; unknown

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

### `notary:server-0.7.0` - linux; arm variant v6

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

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:f9e3c9ec1019bea906aa7405295ecf1381f7f6475f53590adcd15c23d1d0869e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84029b580ae55ba49fd85302ea06cb5cd4e1bed5ac274e721d0f4f0666676711`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
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
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871114d42287b33918110eb07523b39cc14160b33769f724b170bf43a4c2448`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25e6b54e0007f0999c84ca49cf883a52575b965111792bbe02d2f093c96ac81`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c11637e18c4d43df896acfb974619c241e4e37c095aeffeb276ab3a2cdf406`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 4.7 MB (4734451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f419ca26bb54623d108a021c2c2c34eaed1c16f92fa2229285b99b0282256dd`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ace66c72250b80705eea11b9c2d2f3ba3369734a40cd6cd6354470eae494b`  
		Last Modified: Sat, 27 Jan 2024 20:32:28 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:e2b01b3020019bbc8c85dae68cfeb4c58807a7ae34573688b4f46109f7402711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 KB (110568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b16dcbaac1ebcfa1229ae13647f11cfd29977ea29c5999f14fdaa29507e16a6`

```dockerfile
```

-	Layers:
	-	`sha256:8e76965d142c8d838b9c5bb1a2db25f48b35befdf374a819173f93cc04632dd0`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 91.5 KB (91498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61c36adb1e2075dd8b4f29949c82350818cecaa8c296f6d8a94c58990f468575`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 19.1 KB (19070 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:server-0.7.0` - linux; 386

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

### `notary:server-0.7.0` - unknown; unknown

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

### `notary:server-0.7.0` - linux; ppc64le

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

### `notary:server-0.7.0` - unknown; unknown

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

### `notary:server-0.7.0` - linux; s390x

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

### `notary:server-0.7.0` - unknown; unknown

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

## `notary:signer`

```console
$ docker pull notary@sha256:df5da987c4104b15a080e519ac4d33c58716f674d919740baa06301e50a74157
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

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:a4e258f73d4674205beadab255174c4f516c348db847fac094f9363457c46dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe56005d524c90906455ff2818ec543d6125ba6a8fa04eb0b6e3c460d84af02`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ea5704c052c3982b8d4f63ed471b4ab8b74e1f0aa8aa218a53c44bc3be897`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459bd8bdbb874f459723084d5a41e2ab83de68f760d039a964b58330a8b4f07`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67a57cc98df18b03fc342fe8dbd304278b24d35481a79bcdcc91ee4a3d05ebb`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 4.8 MB (4763086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e959da0c342197f160c5cdf24fa0807c2d0b3919204f474cc47cb7f68ec5cb`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e68b02be55bcf47409178c58f683ca36ce4a9a26616f1354513a19b98dc1268`  
		Last Modified: Sat, 27 Jan 2024 00:53:16 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:6ad7d47206e709ba310bf7ab4654d621541ab8573788f914bd20a55ed65ff6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 KB (107290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d02405eba0c306c84d3e92705b4f60c63078bf8f1f22ef4d9455c637ca735eb`

```dockerfile
```

-	Layers:
	-	`sha256:8a8c001633686bbf4f04f9bb8a418789334c15ae7e0401990b23235b00548b79`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 88.0 KB (88044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a3adf6c2eea952cd2f89e4d5a9e88ca2dd1dc1dd9dc471010283077bf80257`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:65861e496c2a89861f24aae1e230413422204f5d85529405e213e137c03ddf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fc96cf0be3836d3e800e2e675a5fa860ab4ac12bed105b2de1d2099dcf6dbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:42f02f663975232742358fed9118fd56abed084a8b0350c9dd332e90c9becea4`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03397ec88fc769559ee4b471e98c53345450eea8a2f0ac146b93cf38b9f3b6cf`  
		Last Modified: Fri, 01 Dec 2023 12:31:43 GMT  
		Size: 4.5 MB (4526083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22e564c80a0e1d630759a8adf2715c6f3e9eea6922d07743cbfca49340c8688`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c311966ad150702a111c2fbfb2141efab1f7b273d7d218d95ac68c55dc840b`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:56ba4141049fb7738bd7ffd13473df498ffa7a9ba62d77f3c35cc3c3cf765bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0839084c88f950d34fcd5df9ec723402893ba5dba5759bd4dfa2bf0ac8cc06bf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871114d42287b33918110eb07523b39cc14160b33769f724b170bf43a4c2448`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410538de933de15c8c872feb53b039d5090f04cbf7b5b48d31eb21346d92e79c`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e6d0e154f38d04ff97de22e704ad8537b2d9f887a891c6a1813b2f201f636`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 4.4 MB (4393060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f28dbc4802c0caa3218e8a055b2df79716e0041a7fa925080e9dbc2167e8bb1`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158b91aa8241285578eff6545cb4043ae4db56453ddbc63513f977d76b8d4ea`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:bf57fde03d0a04eb0304cedb3cef170a8083bac8990afaac825ac5ff221eb107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 KB (106482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37552696de213681e3034666073a74f3c72e726920def6452577ad6899cb164d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c23b87aed798ef74162e46fb233939993124e6dd895d7dbfe326c38e3c706a`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 88.1 KB (88051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1fccc4d2d43a85912ff4b9d9422eb3afc680fda9050e4258c629f89f5b957fb`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:43229c8c5b79185aa28b62cd635e6a767ef2ec466a8625b2f971ca7a386e1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef63a8d74b915fbd393dee94d0a924a3a40777f9c0146f216e65484d77a1f9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:d774e70db794cae73351fd822d82d497ead52871ac6abc00892b9d5df8d14ee9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:f7286662823688d15d8d154fce6a97114514723ec2d9806a9527337308bd4dd9`  
		Last Modified: Sat, 27 Jan 2024 00:39:18 GMT  
		Size: 2.8 MB (2811055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464cc0ec390d581f31adcd0693c24b5e9435dc904dff7a7428887035fb4c3df`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be9c25ec49b01758efe393b242926ed462fe3b2bbae131e0d496d9fb387e95`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2ac4cc17f3cad9b0efb9b356ecbe3de44f7ea6323efbfd44ce637f6b283f7`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 4.6 MB (4579015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1c776e27445d27d902bc87a256b31ef89d7622c350edc7af24c88f57081002`  
		Last Modified: Sat, 27 Jan 2024 01:54:01 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0424e35c8690aaf4303331f2e4d23db1b11b33ec906fbb1fcbe0e1c895de414b`  
		Last Modified: Sat, 27 Jan 2024 01:54:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:e95189884d1639be3b84274cdb12ca81673cffdea127a986df89fe5ab99dec29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 KB (107246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1189787079dd6108c9feeef5348789edeebe9c69ce3ee3217236d26689f55b`

```dockerfile
```

-	Layers:
	-	`sha256:18895a4af3ad85a6cd35f4659a7d1ac77010e597aec3cf7cc177dae0f5170780`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 88.0 KB (88029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1479da16ea7d09df031a06b144fdae6e332a456e473e49df7da3060bd09865b`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 19.2 KB (19217 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:2aa671033b8c981677f54a1a955816ba17022e29ea34c731dd928727efe41435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b934ca82675bc242409ce3effe5c3c870da59797b4795c5701de982cb9ff04c3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:9e1599e40fe1c3eca2e8c8844e5ed20f33c0a09c663ff81b83c6ef38da62b0ea`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19113c8f1ecb888365a3790f47cf4aebb8550741024e85c140ef89ad0570933c`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 4.3 MB (4296967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a98e854f1812325b83d5185f2f0b01a4d4031b3cfa3cb0296613d11efbae3d`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911ecfbc006e1f60d8125ac6058606d7337ae72554f858f5db12b013e49f233`  
		Last Modified: Sat, 27 Jan 2024 10:09:57 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:18a4a001219effc407e78bb00ad50daad58054be5bf87647728ac6dcbb73b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 KB (104890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84d59bbfb301f09d4ceb96cfd4514c25aa6c7c051422d613013b9d51c8683b1`

```dockerfile
```

-	Layers:
	-	`sha256:f30b86170a1c97e33bb2c854853e600912733d0f8c124c2f69c0a2b41f16f0f3`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 86.4 KB (86430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e856cc9774a9ed314b963658cac098d54ca2ff2845415dc5f290f6e983c921`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:23b5119f61f785a5bc3d0e08d81069495e7b7812a69f15f6894ff355737dee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2769d25e3c0fd0dd829d59aeff8c1f0a3ebe2a1bc017678473a5f6f4f3d5df`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:61ca950734db4b88a8271bdb375716842b44f57947be9a32ce1832cc959ce05d`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d0e7d288849a47e06194310df9a8c2bd5638f0c5cce65be749c4da7e6fbf3`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 4.6 MB (4606704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9556c8fc916d6d56403f96617359720b8239dceec8ae11ca4e259228c84f7f1`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0921e503e64d527f3a5b47ee31cc425598e2d4e5f4b074d69210fa19e9f5dbd`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:c84dbdb9b42aafc6e1def960ec053709e57577b1eb06ea6cdb66da0e94acc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d20e11e1a8b94999e93299a89fb110480ceecf6ed20bcaba85641e50c0ca`

```dockerfile
```

-	Layers:
	-	`sha256:0f50abc9fa459207c91633f207420e89dee36d1dec0d0a16ee61f045320df614`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 86.4 KB (86375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3029f7c5714f65e0d9cb914f5bbd69e4a57ef31e8cfa027d7de49000dc85b32`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:df5da987c4104b15a080e519ac4d33c58716f674d919740baa06301e50a74157
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

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:a4e258f73d4674205beadab255174c4f516c348db847fac094f9363457c46dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe56005d524c90906455ff2818ec543d6125ba6a8fa04eb0b6e3c460d84af02`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67ea5704c052c3982b8d4f63ed471b4ab8b74e1f0aa8aa218a53c44bc3be897`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5459bd8bdbb874f459723084d5a41e2ab83de68f760d039a964b58330a8b4f07`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67a57cc98df18b03fc342fe8dbd304278b24d35481a79bcdcc91ee4a3d05ebb`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 4.8 MB (4763086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e959da0c342197f160c5cdf24fa0807c2d0b3919204f474cc47cb7f68ec5cb`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e68b02be55bcf47409178c58f683ca36ce4a9a26616f1354513a19b98dc1268`  
		Last Modified: Sat, 27 Jan 2024 00:53:16 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:6ad7d47206e709ba310bf7ab4654d621541ab8573788f914bd20a55ed65ff6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 KB (107290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d02405eba0c306c84d3e92705b4f60c63078bf8f1f22ef4d9455c637ca735eb`

```dockerfile
```

-	Layers:
	-	`sha256:8a8c001633686bbf4f04f9bb8a418789334c15ae7e0401990b23235b00548b79`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 88.0 KB (88044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a3adf6c2eea952cd2f89e4d5a9e88ca2dd1dc1dd9dc471010283077bf80257`  
		Last Modified: Sat, 27 Jan 2024 00:53:15 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:65861e496c2a89861f24aae1e230413422204f5d85529405e213e137c03ddf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fc96cf0be3836d3e800e2e675a5fa860ab4ac12bed105b2de1d2099dcf6dbb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cde69ed9ff455c9499e13b92a67b8722a1710401c31263561cf43c64193c3d80 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:42f02f663975232742358fed9118fd56abed084a8b0350c9dd332e90c9becea4`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03397ec88fc769559ee4b471e98c53345450eea8a2f0ac146b93cf38b9f3b6cf`  
		Last Modified: Fri, 01 Dec 2023 12:31:43 GMT  
		Size: 4.5 MB (4526083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22e564c80a0e1d630759a8adf2715c6f3e9eea6922d07743cbfca49340c8688`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c311966ad150702a111c2fbfb2141efab1f7b273d7d218d95ac68c55dc840b`  
		Last Modified: Fri, 01 Dec 2023 12:31:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:56ba4141049fb7738bd7ffd13473df498ffa7a9ba62d77f3c35cc3c3cf765bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0839084c88f950d34fcd5df9ec723402893ba5dba5759bd4dfa2bf0ac8cc06bf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871114d42287b33918110eb07523b39cc14160b33769f724b170bf43a4c2448`  
		Last Modified: Sat, 27 Jan 2024 20:32:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410538de933de15c8c872feb53b039d5090f04cbf7b5b48d31eb21346d92e79c`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3e6d0e154f38d04ff97de22e704ad8537b2d9f887a891c6a1813b2f201f636`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 4.4 MB (4393060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f28dbc4802c0caa3218e8a055b2df79716e0041a7fa925080e9dbc2167e8bb1`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b158b91aa8241285578eff6545cb4043ae4db56453ddbc63513f977d76b8d4ea`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:bf57fde03d0a04eb0304cedb3cef170a8083bac8990afaac825ac5ff221eb107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 KB (106482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37552696de213681e3034666073a74f3c72e726920def6452577ad6899cb164d`

```dockerfile
```

-	Layers:
	-	`sha256:b3c23b87aed798ef74162e46fb233939993124e6dd895d7dbfe326c38e3c706a`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 88.1 KB (88051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1fccc4d2d43a85912ff4b9d9422eb3afc680fda9050e4258c629f89f5b957fb`  
		Last Modified: Sat, 27 Jan 2024 20:32:45 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:43229c8c5b79185aa28b62cd635e6a767ef2ec466a8625b2f971ca7a386e1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef63a8d74b915fbd393dee94d0a924a3a40777f9c0146f216e65484d77a1f9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:d774e70db794cae73351fd822d82d497ead52871ac6abc00892b9d5df8d14ee9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:f7286662823688d15d8d154fce6a97114514723ec2d9806a9527337308bd4dd9`  
		Last Modified: Sat, 27 Jan 2024 00:39:18 GMT  
		Size: 2.8 MB (2811055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4464cc0ec390d581f31adcd0693c24b5e9435dc904dff7a7428887035fb4c3df`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be9c25ec49b01758efe393b242926ed462fe3b2bbae131e0d496d9fb387e95`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd2ac4cc17f3cad9b0efb9b356ecbe3de44f7ea6323efbfd44ce637f6b283f7`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 4.6 MB (4579015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1c776e27445d27d902bc87a256b31ef89d7622c350edc7af24c88f57081002`  
		Last Modified: Sat, 27 Jan 2024 01:54:01 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0424e35c8690aaf4303331f2e4d23db1b11b33ec906fbb1fcbe0e1c895de414b`  
		Last Modified: Sat, 27 Jan 2024 01:54:01 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:e95189884d1639be3b84274cdb12ca81673cffdea127a986df89fe5ab99dec29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 KB (107246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1189787079dd6108c9feeef5348789edeebe9c69ce3ee3217236d26689f55b`

```dockerfile
```

-	Layers:
	-	`sha256:18895a4af3ad85a6cd35f4659a7d1ac77010e597aec3cf7cc177dae0f5170780`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 88.0 KB (88029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1479da16ea7d09df031a06b144fdae6e332a456e473e49df7da3060bd09865b`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 19.2 KB (19217 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:2aa671033b8c981677f54a1a955816ba17022e29ea34c731dd928727efe41435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b934ca82675bc242409ce3effe5c3c870da59797b4795c5701de982cb9ff04c3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:9e1599e40fe1c3eca2e8c8844e5ed20f33c0a09c663ff81b83c6ef38da62b0ea`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19113c8f1ecb888365a3790f47cf4aebb8550741024e85c140ef89ad0570933c`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 4.3 MB (4296967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a98e854f1812325b83d5185f2f0b01a4d4031b3cfa3cb0296613d11efbae3d`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911ecfbc006e1f60d8125ac6058606d7337ae72554f858f5db12b013e49f233`  
		Last Modified: Sat, 27 Jan 2024 10:09:57 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:18a4a001219effc407e78bb00ad50daad58054be5bf87647728ac6dcbb73b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 KB (104890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84d59bbfb301f09d4ceb96cfd4514c25aa6c7c051422d613013b9d51c8683b1`

```dockerfile
```

-	Layers:
	-	`sha256:f30b86170a1c97e33bb2c854853e600912733d0f8c124c2f69c0a2b41f16f0f3`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 86.4 KB (86430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e856cc9774a9ed314b963658cac098d54ca2ff2845415dc5f290f6e983c921`  
		Last Modified: Sat, 27 Jan 2024 10:09:56 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:23b5119f61f785a5bc3d0e08d81069495e7b7812a69f15f6894ff355737dee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2769d25e3c0fd0dd829d59aeff8c1f0a3ebe2a1bc017678473a5f6f4f3d5df`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:f7a7034bb4c8ab0fed6e2c4b09f15f3e7076270496340adceac7e01aabf87857 in / 
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["/bin/sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 24 Oct 2022 22:10:44 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
WORKDIR /notary/signer
# Mon, 24 Oct 2022 22:10:44 GMT
COPY /notary-signer ./ # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
RUN ./notary-signer --version # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./signer-config.json . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 24 Oct 2022 22:10:44 GMT
USER notary
# Mon, 24 Oct 2022 22:10:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 24 Oct 2022 22:10:44 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:61ca950734db4b88a8271bdb375716842b44f57947be9a32ce1832cc959ce05d`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d0e7d288849a47e06194310df9a8c2bd5638f0c5cce65be749c4da7e6fbf3`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 4.6 MB (4606704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9556c8fc916d6d56403f96617359720b8239dceec8ae11ca4e259228c84f7f1`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0921e503e64d527f3a5b47ee31cc425598e2d4e5f4b074d69210fa19e9f5dbd`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:c84dbdb9b42aafc6e1def960ec053709e57577b1eb06ea6cdb66da0e94acc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89d20e11e1a8b94999e93299a89fb110480ceecf6ed20bcaba85641e50c0ca`

```dockerfile
```

-	Layers:
	-	`sha256:0f50abc9fa459207c91633f207420e89dee36d1dec0d0a16ee61f045320df614`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 86.4 KB (86375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3029f7c5714f65e0d9cb914f5bbd69e4a57ef31e8cfa027d7de49000dc85b32`  
		Last Modified: Fri, 01 Dec 2023 11:05:45 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
