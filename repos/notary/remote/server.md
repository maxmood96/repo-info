## `notary:server`

```console
$ docker pull notary@sha256:5e27de0e16fb39867759d9785d942dfae12745c958e2450bd1c80cc82e80903c
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
$ docker pull notary@sha256:c4589237d14cd12decc4491a981fd2b3f8e33e3d4723529e7ab90305f02ad355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969de5928915e69d71318e0034e2323d830c7fee962e47f3415fac64dcf681b5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b9d7ac5ec01e1212e2bab28ec95c28e4f9705a2c0d0b65a2d381dd75da59f65a in / 
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
	-	`sha256:a7f1ea9eab1fb2b4aeff039474a8ee96afa63468cf85726a63ed8c31e861476d`  
		Last Modified: Sat, 27 Jan 2024 00:43:40 GMT  
		Size: 2.6 MB (2592124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e4fcd23a75ab498c139f1a2a88ec5200c49da4be978f6b30a8f1c5509d8c5`  
		Last Modified: Sun, 28 Jan 2024 10:21:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de984f719a5a37c8bf21f0b37d5c93f947beddff73f8513af667d3ab21a88281`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 118.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9aaedeba9ceed57c1088c9fef919efb2ece379921d43d401f0eedf54aebfa8`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 5.0 MB (4976492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df625dbb8764e4666ee098bc2e561fdbd9eea57cebec718f94ef916fa35f35`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c541579ca238d10eb1822fe04e5dad184499952c707decdf4dcf51b85d90b30`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:34372f22fefe2f5c5d8d678828b97b109bf16dc4f78430d32c2503f0ba28013a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 KB (108919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4497c13ba6abce3e8f4c40189b89e6b34b86592d26f7970762f33a6117ef73b`

```dockerfile
```

-	Layers:
	-	`sha256:fd486e7b1555837b8e08d993a8a016d0f21b2e08ce1b40ca85871ba42cadc4d6`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7ac420fb5e3f9fb31d136996c54b5e6845efa356e2324f9693f79666819215`  
		Last Modified: Sun, 28 Jan 2024 10:21:18 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json
