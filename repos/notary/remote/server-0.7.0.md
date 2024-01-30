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
