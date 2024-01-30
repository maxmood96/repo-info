<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:adf20b4f0a05cf8b44b095d877664358917098779795e8a36fbaa78901826bae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
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
$ docker pull notary@sha256:c6f74294aee419c7b22194def439ea1b496cc9021e5270fb80d7954864e39e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5d21960c6c84cdf6e9327b3f8d54289c302173f9cb34a8297c59586a743a8c`
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
	-	`sha256:a1f8f2bf6fa05d877fa8ce8870835fa94a2f025220fb6d48c8203f87a998bbe2`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d1dea302c459ab4660869cfe6accf625525f1aeeeacc64cc2f3dedda5bdd04`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796ead184d4ba893bb4c2af84e14d48c1157d1cc4697d7e216620816e7c4b1fc`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 5.1 MB (5147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5f8fbf76e9d3e96ae78db5a561847fb995bce94d259a399fe9af29ecbde6a4`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ebeb50b486b00b172f091cc0dd022ba70dca2d1b1c99e0aa0bbe40360575af`  
		Last Modified: Tue, 30 Jan 2024 20:31:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:ce18cfb6aab080f86ec811522b92560ad8d73d0aaa5580f1f78ed35a72c9d76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 KB (118943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c85a643754997bb4e41a25002ddec38a103fc3cd8abdb6409b503bb1b84c170`

```dockerfile
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
```

-	Layers:
	-	`sha256:c97dc518cf3c79d34aa2899a1257f6b285044102c4ea02423b6763fbbfb99ef7`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 91.5 KB (91491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb8dbdeb90ba5c910012c42db99e9871c4f8588b52f061a57d3201ef074607e`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40427ae301147ffe3a654227a343ea331cdd5f22ab2d9adb1f94df5175a39094`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse
	-	`sha256:a5c1c3f53126fa0d78fa296310d1504c32e8ddef798c239586d8d043de67a645`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:27eeb5fa2ad1a0d82ffec781e37b071ef7111918a67df7d288382dcef47ff640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b5ca69449d40d149071a52290c54c7815d33b1d6ed7efa88d26fae0e223b41`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
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
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74657dd1e96df2c28f1594d3eada4cc7e83a21c56c0523cb474fccd867dab4`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eadda8e880d785961a1c13b8375f9992e9ebf77d75b5e1356f4d2d6a37a6dc`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb621b3714eeb12ce31453b3c373a22b7ef1059f3c05e0bb671fb12d6ad93c06`  
		Last Modified: Tue, 30 Jan 2024 18:57:13 GMT  
		Size: 4.9 MB (4893568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33754574e7de01a162d8051349c9e11c5aa0f580864b9453cf2c0540819b531`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675f301c102b3dc063bd64de3b66b24c78e53b922640120d1823ffd42384b2`  
		Last Modified: Tue, 30 Jan 2024 18:57:13 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server` - unknown; unknown

```console
$ docker pull notary@sha256:0443143bdbc03559cf891500e5f62d0a18dcb581015139832017282c2bf3c8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028d94f6529a6aa8fe51ce446fdc8d8fd78a8dc479fa493dcf76b7d4a3a3fb9a`

```dockerfile
```

-	Layers:
	-	`sha256:6bae0458374e9dc37d3d298381cb973e3664322f7a0f29c593dd0fad3c966442`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 19.0 KB (18958 bytes)  
		MIME: application/vnd.in-toto+json

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

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:adf20b4f0a05cf8b44b095d877664358917098779795e8a36fbaa78901826bae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
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
$ docker pull notary@sha256:c6f74294aee419c7b22194def439ea1b496cc9021e5270fb80d7954864e39e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5d21960c6c84cdf6e9327b3f8d54289c302173f9cb34a8297c59586a743a8c`
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
	-	`sha256:a1f8f2bf6fa05d877fa8ce8870835fa94a2f025220fb6d48c8203f87a998bbe2`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d1dea302c459ab4660869cfe6accf625525f1aeeeacc64cc2f3dedda5bdd04`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 117.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796ead184d4ba893bb4c2af84e14d48c1157d1cc4697d7e216620816e7c4b1fc`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 5.1 MB (5147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5f8fbf76e9d3e96ae78db5a561847fb995bce94d259a399fe9af29ecbde6a4`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ebeb50b486b00b172f091cc0dd022ba70dca2d1b1c99e0aa0bbe40360575af`  
		Last Modified: Tue, 30 Jan 2024 20:31:36 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:ce18cfb6aab080f86ec811522b92560ad8d73d0aaa5580f1f78ed35a72c9d76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 KB (118943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c85a643754997bb4e41a25002ddec38a103fc3cd8abdb6409b503bb1b84c170`

```dockerfile
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
# Mon, 01 Jan 2001 00:00:00 GMT
RUN 
```

-	Layers:
	-	`sha256:c97dc518cf3c79d34aa2899a1257f6b285044102c4ea02423b6763fbbfb99ef7`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 91.5 KB (91491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb8dbdeb90ba5c910012c42db99e9871c4f8588b52f061a57d3201ef074607e`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40427ae301147ffe3a654227a343ea331cdd5f22ab2d9adb1f94df5175a39094`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse
	-	`sha256:a5c1c3f53126fa0d78fa296310d1504c32e8ddef798c239586d8d043de67a645`  
		Last Modified: Tue, 30 Jan 2024 20:31:35 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.oci.descriptor.v1+json+dsse

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:27eeb5fa2ad1a0d82ffec781e37b071ef7111918a67df7d288382dcef47ff640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b5ca69449d40d149071a52290c54c7815d33b1d6ed7efa88d26fae0e223b41`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
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
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74657dd1e96df2c28f1594d3eada4cc7e83a21c56c0523cb474fccd867dab4`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eadda8e880d785961a1c13b8375f9992e9ebf77d75b5e1356f4d2d6a37a6dc`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb621b3714eeb12ce31453b3c373a22b7ef1059f3c05e0bb671fb12d6ad93c06`  
		Last Modified: Tue, 30 Jan 2024 18:57:13 GMT  
		Size: 4.9 MB (4893568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33754574e7de01a162d8051349c9e11c5aa0f580864b9453cf2c0540819b531`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44675f301c102b3dc063bd64de3b66b24c78e53b922640120d1823ffd42384b2`  
		Last Modified: Tue, 30 Jan 2024 18:57:13 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:server-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:0443143bdbc03559cf891500e5f62d0a18dcb581015139832017282c2bf3c8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028d94f6529a6aa8fe51ce446fdc8d8fd78a8dc479fa493dcf76b7d4a3a3fb9a`

```dockerfile
```

-	Layers:
	-	`sha256:6bae0458374e9dc37d3d298381cb973e3664322f7a0f29c593dd0fad3c966442`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 19.0 KB (18958 bytes)  
		MIME: application/vnd.in-toto+json

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

### `notary:server-0.7.0` - unknown; unknown

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

## `notary:signer`

```console
$ docker pull notary@sha256:138f938ec5b0f127911b1a63aa41c92131d162fdd3c384425ce63c4b19aaf912
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
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
$ docker pull notary@sha256:aeaebe6db1cb96d37f70a2fead0b67392ba45976d81e7b2960f9ae386c1ff60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707b5a55c925b32e171ec8180da7559982e75199866fc624886353b0c8068b65`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
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
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74657dd1e96df2c28f1594d3eada4cc7e83a21c56c0523cb474fccd867dab4`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5e0de0f41694c6ad3e7e51c4169271f7ed41164469eb2c58e3016f3df5a76`  
		Last Modified: Tue, 30 Jan 2024 18:57:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45013e3a8f272dedb2d12cd13a6ae2c4d7e4b8954b331959e8b7697e334f691b`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 4.5 MB (4526085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497332bdba601b361bbc21d6a5f80bcd48d80bf093623867bcf738985c32615`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c382fb4ce798e366082f207e7e1c7dad0e1d3542e556f09db7573909f0962018`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:1191650cd9fcd22e23d16ffae6f4e318924dec99403d74e89ee24a09ddf18be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2943c57d34ac80a49eb5694f30352474c1613b729c440597bd8de013bb1d997f`

```dockerfile
```

-	Layers:
	-	`sha256:3bd2e6a70074f99ce6e977f4c3d67794009a984ab89dd45bb07d4769547b14a2`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull notary@sha256:948a1e492bf8a8acfb50ab469d196def8e9c0067b6ba6638be96fcf5e8be38c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b013bf38fa165b3a0efcb803352b6dba52a1dc46b6d49ac5e12c1216e5c124`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b9d7ac5ec01e1212e2bab28ec95c28e4f9705a2c0d0b65a2d381dd75da59f65a in / 
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
	-	`sha256:a7f1ea9eab1fb2b4aeff039474a8ee96afa63468cf85726a63ed8c31e861476d`  
		Last Modified: Sat, 27 Jan 2024 00:43:40 GMT  
		Size: 2.6 MB (2592124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e4fcd23a75ab498c139f1a2a88ec5200c49da4be978f6b30a8f1c5509d8c5`  
		Last Modified: Sun, 28 Jan 2024 10:21:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b6dc6776403949de2056b9a44f45d62a49667d6e251c13d5358c5cf5df82b0`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd43f00868ac9c01f84b005bf43517b633cf861aef36c373b386b5411de4108`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 4.6 MB (4606699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6ab9d90cdcc590780240eec3758ec407de20dbee201426247711decdf96be`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56d00e6d9c7e85947fd8406dd9d17f21b08e532fd66a4a3619133f8b82c1a9`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer` - unknown; unknown

```console
$ docker pull notary@sha256:14ea2782ef369e9f938009c6758894f4265348da6f5e3e2ac39318d073c046d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de48d74efbafdf2d12e2da9c741a467fd5bdeb2728c60940c8e0d38bf1048f56`

```dockerfile
```

-	Layers:
	-	`sha256:517239ce0f7e70d4ab9559e95222a78793405d8ce1bd1a2af0a18877996d9961`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 86.4 KB (86408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3a1811181c41623a54c1a89a7b883647dd0c8f3a8fb65e0f99b37441dfff05`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:138f938ec5b0f127911b1a63aa41c92131d162fdd3c384425ce63c4b19aaf912
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
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
$ docker pull notary@sha256:aeaebe6db1cb96d37f70a2fead0b67392ba45976d81e7b2960f9ae386c1ff60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707b5a55c925b32e171ec8180da7559982e75199866fc624886353b0c8068b65`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
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
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74657dd1e96df2c28f1594d3eada4cc7e83a21c56c0523cb474fccd867dab4`  
		Last Modified: Tue, 30 Jan 2024 18:57:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5e0de0f41694c6ad3e7e51c4169271f7ed41164469eb2c58e3016f3df5a76`  
		Last Modified: Tue, 30 Jan 2024 18:57:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45013e3a8f272dedb2d12cd13a6ae2c4d7e4b8954b331959e8b7697e334f691b`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 4.5 MB (4526085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3497332bdba601b361bbc21d6a5f80bcd48d80bf093623867bcf738985c32615`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c382fb4ce798e366082f207e7e1c7dad0e1d3542e556f09db7573909f0962018`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:1191650cd9fcd22e23d16ffae6f4e318924dec99403d74e89ee24a09ddf18be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2943c57d34ac80a49eb5694f30352474c1613b729c440597bd8de013bb1d997f`

```dockerfile
```

-	Layers:
	-	`sha256:3bd2e6a70074f99ce6e977f4c3d67794009a984ab89dd45bb07d4769547b14a2`  
		Last Modified: Tue, 30 Jan 2024 18:57:31 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull notary@sha256:948a1e492bf8a8acfb50ab469d196def8e9c0067b6ba6638be96fcf5e8be38c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b013bf38fa165b3a0efcb803352b6dba52a1dc46b6d49ac5e12c1216e5c124`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 24 Oct 2022 22:10:44 GMT
ADD file:b9d7ac5ec01e1212e2bab28ec95c28e4f9705a2c0d0b65a2d381dd75da59f65a in / 
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
	-	`sha256:a7f1ea9eab1fb2b4aeff039474a8ee96afa63468cf85726a63ed8c31e861476d`  
		Last Modified: Sat, 27 Jan 2024 00:43:40 GMT  
		Size: 2.6 MB (2592124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e4fcd23a75ab498c139f1a2a88ec5200c49da4be978f6b30a8f1c5509d8c5`  
		Last Modified: Sun, 28 Jan 2024 10:21:17 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b6dc6776403949de2056b9a44f45d62a49667d6e251c13d5358c5cf5df82b0`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd43f00868ac9c01f84b005bf43517b633cf861aef36c373b386b5411de4108`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 4.6 MB (4606699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6ab9d90cdcc590780240eec3758ec407de20dbee201426247711decdf96be`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a56d00e6d9c7e85947fd8406dd9d17f21b08e532fd66a4a3619133f8b82c1a9`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `notary:signer-0.7.0` - unknown; unknown

```console
$ docker pull notary@sha256:14ea2782ef369e9f938009c6758894f4265348da6f5e3e2ac39318d073c046d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 KB (104833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de48d74efbafdf2d12e2da9c741a467fd5bdeb2728c60940c8e0d38bf1048f56`

```dockerfile
```

-	Layers:
	-	`sha256:517239ce0f7e70d4ab9559e95222a78793405d8ce1bd1a2af0a18877996d9961`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 86.4 KB (86408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3a1811181c41623a54c1a89a7b883647dd0c8f3a8fb65e0f99b37441dfff05`  
		Last Modified: Sun, 28 Jan 2024 10:24:01 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json
