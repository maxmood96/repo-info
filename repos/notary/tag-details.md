<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:1c89c24386f5d24f3d4eaafa0ecfa0f1ae410fef67106ed3fe97101b22aad6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:e08e171973bd0aa3eff9d3bd360f28ca94c8322bf3cdaa05ce304202c32ca0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb8ff7a20dddff08c544af63662a7767191bed486376d2ab28c9f6f4ddf7e45`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
USER notary
# Wed, 29 Mar 2023 18:19:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0647f7d50bd9007a9af72eec9925f5e3e4e0c35d1796c4a0970fca9f7c127a2a`  
		Last Modified: Wed, 29 Mar 2023 19:31:54 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb624cd06df602b5b41078cd8459f5f9cfbae1af96449820dfebaebf8e32c`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e233daeba067abd69c49dee76b909ea17108e6b329e4a6ed9b854b3bd460896`  
		Last Modified: Wed, 29 Mar 2023 19:31:53 GMT  
		Size: 5.1 MB (5147062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7b5e900feac98630483fb723364bb4e990711776e05522c09f14e48912f6c`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 89.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72f25e33f6fc2c5ea648b20c45299a45987e976104f304b5a6b2644558603fc`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4c2871cb69cc4df46a7fda38662fc19d65ca65ac8b83f17a476bd5afb2314a`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:23d915b8fc86ba84a47569759c085a1fce986718b48ed6c3798edc7f92865eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c51aedff3c3e5ac57a0ff65372e9ae7a6ea98548e62e4c9354c6ffe2bf1c8f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214377c027ebc3bfa8cf5d9c6adfe42cde43421c65fc600f490de087016f240c`  
		Last Modified: Wed, 08 Mar 2023 00:17:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3bb2a4e62a65feb82fba8588770b570f54113f46f523b08f7818828fa53331`  
		Last Modified: Tue, 28 Mar 2023 00:20:59 GMT  
		Size: 4.9 MB (4891950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff8843aea5a062ff464e1104d4cb83972aaa0839fc7d62c2a9775ed52d1fbf`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d263be01dcc7d5866ad1c9c9ed1ef5740967e63099e03f6b85a3e1f72749d9e6`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd4b4ae5f17d4495c678e86f290ed0dad3c41e9926c582bb4526c43c39e67fd`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:606473b36fe802565fc6cd44209c42a4fe7dfd6016882f894307eb6955231024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b18a624856d85f846a744f1c712e00e1b6f122fbaba207d81676636fdb4c90`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
USER notary
# Wed, 29 Mar 2023 17:39:20 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b02441c89b609b85e27619f8e09f858e27fdac246a198c3e19163753fcb092`  
		Last Modified: Wed, 29 Mar 2023 21:25:30 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be341198c2c1024a88bf425d3d85938636d2f2245ff653215d9656b0c95a9867`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ad3f2412b6448f1df98eb98f1226c1f7a879c65c64bd6d732037ae7f0b042`  
		Last Modified: Wed, 29 Mar 2023 21:25:29 GMT  
		Size: 4.7 MB (4732799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252bb73eb328068738028c333212224abba0ed43a7a98c38bfe227ed6f8f3c73`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442befcb309f4a843c266f51793b206eec0f7bc70de776bc4e5fbb52a22b7d4`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e6aa23c1fed18306af3eb0c8231a1ce778f92ecd35c12ead8cd4289c54f37b`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:3bbc97281bffc2fd362257fd87ba108bc61912f8b963047bd81770d9f9340a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c272e6034e8c04514730a63792c6d7d6add1e4aa56b057cead31d50a6f106fa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
USER notary
# Wed, 29 Mar 2023 18:08:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fe6407f813eee3328c3e3f4bbd5ee13b51acde95006059cfb731f7988943bc`  
		Last Modified: Wed, 29 Mar 2023 20:02:06 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d063664bd25326f6e9c648afcdb1d8586b5b6498dfe6770038000947c8f935`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad33646a6a6184efef697df6bf3433747f0e4ce2e91064f893d6b71ec5c05f47`  
		Last Modified: Wed, 29 Mar 2023 20:02:05 GMT  
		Size: 4.9 MB (4948877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ce6abf2fcd69d86efd2d762564c115c8ab639114b0ef47a01f50eb95bd6d0`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132aaa5c1be8694f33c9b0f457252a91da484ebfab818f920dca166449c3806a`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227623bd304a4e813c69bfadb810b933ff3327addba2ce02b3cb98f0b89308cc`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:bf93f2004a01468ef671769d44fe092eb46dda89cac9de3aab943d61a7933a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0e629b4c721cfc24c915404f65be4e4b4f09e7ae0ad67ee65c9b29fd16155a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
USER notary
# Mon, 27 Mar 2023 22:22:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17b8bc3dd04442591c8af362c063ac63f5cf8890143e98399dcc289f1979b12`  
		Last Modified: Sat, 11 Feb 2023 09:33:08 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84ab3ea445bf8905993342ed5e14c11b723eaa755896fe54226877282a0e02a`  
		Last Modified: Tue, 28 Mar 2023 02:19:32 GMT  
		Size: 4.6 MB (4637491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5e82ca9b473569d5a0b8e0b790e851b70b7611e667a534b00f724a7c1944c5`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bede979fcc8661ed27bf1d48aa17c21f493159dc6d45f8a6f793d799cecaf7de`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bb99bb39c06c3637ae02706a09496c42a866e29c30b7acf624fa53408ab897`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:9b7c56530b43401e1f45e426fb4a4bddcdb1de482f516c888eb34b7346e93add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfc38852de6fa0f7b0c4f34248b015a3f32d192608673170aa75b641df02c58`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
USER notary
# Wed, 29 Mar 2023 17:42:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496bacdc3e38b8319b094c7cd682983189e795236b61f362a29c0e8e94ceb5`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df35cdffecfe59047614da00e02372516c2bc15ab6db89203a960b5357c45501`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc866ec8180777323d59e866dd9c2d6ec2267b6b6005392296dc5a637592bf2`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 5.0 MB (4974125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5e55d8e5289300cbdd726947b9c3045c46f28cd00fed80379f4e309cca44be`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3636bdc70b158e42f2ef819ac582a0b7a32ce32bf22aba65e23f5c38cbfbf5`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11c31727c61b1dedfa04a92f42f5ecdf7cd09305d8812fa0f6ca057d1f16723`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:1c89c24386f5d24f3d4eaafa0ecfa0f1ae410fef67106ed3fe97101b22aad6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:e08e171973bd0aa3eff9d3bd360f28ca94c8322bf3cdaa05ce304202c32ca0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb8ff7a20dddff08c544af63662a7767191bed486376d2ab28c9f6f4ddf7e45`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 18:19:28 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
USER notary
# Wed, 29 Mar 2023 18:19:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0647f7d50bd9007a9af72eec9925f5e3e4e0c35d1796c4a0970fca9f7c127a2a`  
		Last Modified: Wed, 29 Mar 2023 19:31:54 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb624cd06df602b5b41078cd8459f5f9cfbae1af96449820dfebaebf8e32c`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e233daeba067abd69c49dee76b909ea17108e6b329e4a6ed9b854b3bd460896`  
		Last Modified: Wed, 29 Mar 2023 19:31:53 GMT  
		Size: 5.1 MB (5147062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae7b5e900feac98630483fb723364bb4e990711776e05522c09f14e48912f6c`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 89.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72f25e33f6fc2c5ea648b20c45299a45987e976104f304b5a6b2644558603fc`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4c2871cb69cc4df46a7fda38662fc19d65ca65ac8b83f17a476bd5afb2314a`  
		Last Modified: Wed, 29 Mar 2023 19:31:52 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:23d915b8fc86ba84a47569759c085a1fce986718b48ed6c3798edc7f92865eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c51aedff3c3e5ac57a0ff65372e9ae7a6ea98548e62e4c9354c6ffe2bf1c8f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214377c027ebc3bfa8cf5d9c6adfe42cde43421c65fc600f490de087016f240c`  
		Last Modified: Wed, 08 Mar 2023 00:17:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3bb2a4e62a65feb82fba8588770b570f54113f46f523b08f7818828fa53331`  
		Last Modified: Tue, 28 Mar 2023 00:20:59 GMT  
		Size: 4.9 MB (4891950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff8843aea5a062ff464e1104d4cb83972aaa0839fc7d62c2a9775ed52d1fbf`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d263be01dcc7d5866ad1c9c9ed1ef5740967e63099e03f6b85a3e1f72749d9e6`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd4b4ae5f17d4495c678e86f290ed0dad3c41e9926c582bb4526c43c39e67fd`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:606473b36fe802565fc6cd44209c42a4fe7dfd6016882f894307eb6955231024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b18a624856d85f846a744f1c712e00e1b6f122fbaba207d81676636fdb4c90`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 17:39:20 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
USER notary
# Wed, 29 Mar 2023 17:39:20 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b02441c89b609b85e27619f8e09f858e27fdac246a198c3e19163753fcb092`  
		Last Modified: Wed, 29 Mar 2023 21:25:30 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be341198c2c1024a88bf425d3d85938636d2f2245ff653215d9656b0c95a9867`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1ad3f2412b6448f1df98eb98f1226c1f7a879c65c64bd6d732037ae7f0b042`  
		Last Modified: Wed, 29 Mar 2023 21:25:29 GMT  
		Size: 4.7 MB (4732799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252bb73eb328068738028c333212224abba0ed43a7a98c38bfe227ed6f8f3c73`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c442befcb309f4a843c266f51793b206eec0f7bc70de776bc4e5fbb52a22b7d4`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e6aa23c1fed18306af3eb0c8231a1ce778f92ecd35c12ead8cd4289c54f37b`  
		Last Modified: Wed, 29 Mar 2023 21:25:28 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:3bbc97281bffc2fd362257fd87ba108bc61912f8b963047bd81770d9f9340a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c272e6034e8c04514730a63792c6d7d6add1e4aa56b057cead31d50a6f106fa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 18:08:35 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
USER notary
# Wed, 29 Mar 2023 18:08:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fe6407f813eee3328c3e3f4bbd5ee13b51acde95006059cfb731f7988943bc`  
		Last Modified: Wed, 29 Mar 2023 20:02:06 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d063664bd25326f6e9c648afcdb1d8586b5b6498dfe6770038000947c8f935`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad33646a6a6184efef697df6bf3433747f0e4ce2e91064f893d6b71ec5c05f47`  
		Last Modified: Wed, 29 Mar 2023 20:02:05 GMT  
		Size: 4.9 MB (4948877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442ce6abf2fcd69d86efd2d762564c115c8ab639114b0ef47a01f50eb95bd6d0`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132aaa5c1be8694f33c9b0f457252a91da484ebfab818f920dca166449c3806a`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227623bd304a4e813c69bfadb810b933ff3327addba2ce02b3cb98f0b89308cc`  
		Last Modified: Wed, 29 Mar 2023 20:02:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:bf93f2004a01468ef671769d44fe092eb46dda89cac9de3aab943d61a7933a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0e629b4c721cfc24c915404f65be4e4b4f09e7ae0ad67ee65c9b29fd16155a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:22:31 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
USER notary
# Mon, 27 Mar 2023 22:22:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17b8bc3dd04442591c8af362c063ac63f5cf8890143e98399dcc289f1979b12`  
		Last Modified: Sat, 11 Feb 2023 09:33:08 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84ab3ea445bf8905993342ed5e14c11b723eaa755896fe54226877282a0e02a`  
		Last Modified: Tue, 28 Mar 2023 02:19:32 GMT  
		Size: 4.6 MB (4637491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5e82ca9b473569d5a0b8e0b790e851b70b7611e667a534b00f724a7c1944c5`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bede979fcc8661ed27bf1d48aa17c21f493159dc6d45f8a6f793d799cecaf7de`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bb99bb39c06c3637ae02706a09496c42a866e29c30b7acf624fa53408ab897`  
		Last Modified: Tue, 28 Mar 2023 02:19:30 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:9b7c56530b43401e1f45e426fb4a4bddcdb1de482f516c888eb34b7346e93add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfc38852de6fa0f7b0c4f34248b015a3f32d192608673170aa75b641df02c58`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
ENV INSTALLDIR=/notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
WORKDIR /notary/server
# Wed, 29 Mar 2023 17:42:02 GMT
COPY /notary-server ./ # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
RUN ./notary-server --version # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./server-config.json . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
USER notary
# Wed, 29 Mar 2023 17:42:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496bacdc3e38b8319b094c7cd682983189e795236b61f362a29c0e8e94ceb5`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df35cdffecfe59047614da00e02372516c2bc15ab6db89203a960b5357c45501`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc866ec8180777323d59e866dd9c2d6ec2267b6b6005392296dc5a637592bf2`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 5.0 MB (4974125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5e55d8e5289300cbdd726947b9c3045c46f28cd00fed80379f4e309cca44be`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3636bdc70b158e42f2ef819ac582a0b7a32ce32bf22aba65e23f5c38cbfbf5`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11c31727c61b1dedfa04a92f42f5ecdf7cd09305d8812fa0f6ca057d1f16723`  
		Last Modified: Wed, 29 Mar 2023 19:02:12 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:242b047aad4166071a9fc78cebb537d5cf1b448900a50d3243c35153fec52cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:82e6cd74a4dd40ffa22a7171e7fd0a013e59f87577b37bd82089cc62cf48bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08054659a657d14063d1a7d6e89021e83b764bba98b922fe7c4d07cfc7535454`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
USER notary
# Wed, 29 Mar 2023 18:19:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0647f7d50bd9007a9af72eec9925f5e3e4e0c35d1796c4a0970fca9f7c127a2a`  
		Last Modified: Wed, 29 Mar 2023 19:31:54 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0616adcfb81a6d2087ac3d3915f5ffdfe33d1df0716cfc8fc50c4060d9cfbfa`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a5272838ec44589c294ff87c9fed67ea835505803f114918c0e9d078c75d6c`  
		Last Modified: Wed, 29 Mar 2023 19:32:03 GMT  
		Size: 4.8 MB (4761329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9029690a2f5060d5204b6e65bbe79c9584edc7f2dd4c0ad30904d9e788c1cb6c`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 89.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da760519592321c41dd788dd127d45f8add2a4af924d0d60c269af2b17fc68`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c054a9bc9cb6a5f4374f9fc7c2bcdd000d44a564df84e863e7447702fdcbda`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:1b859eda30eea52686ca1e25104c8f6c54b7a110e709d1a4f318ea05c4fc28fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8544b97c1f8075ef86c3cd4f54f6e27fde1a0da79ab270f04d28b956cb23bb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8867bd3aa695c936397740852a2a23245f7a8147431da0dea7ea79cb52c3fb7`  
		Last Modified: Wed, 08 Mar 2023 00:17:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46389c4cd7729b78c0a52df7daa142aedd2c1e21f6d97ff7ebd1a32b0936e54`  
		Last Modified: Tue, 28 Mar 2023 00:21:07 GMT  
		Size: 4.5 MB (4524262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7249b0975a56b424c7ef1643a7155c785f29e8785efa46c4d98c1db7be99ef`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4071d49d37fd4ab8f37c67b5104e1db516290ac99a3c7776fdaa98b1a113af66`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52c19763db6fc8e5bce84d899dd56c58e816226c24f2804400fba9ec85ec9a0`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:10c586a083e1cf792bb6b0682382049a016d694026a180b33c4c6318518fccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029d8b16e8f0c4de8efb5bcd1c92443c642a4304b88a248e0b001fb2c565535c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
USER notary
# Wed, 29 Mar 2023 17:39:20 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b02441c89b609b85e27619f8e09f858e27fdac246a198c3e19163753fcb092`  
		Last Modified: Wed, 29 Mar 2023 21:25:30 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dd30044d17dd0900f33ee4cd64e106aa2d710607e560c51ad8bc6fd3172e8e`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118ec6fe198848420882ff6a719579c9fa2b092eaa7f4aa4ea4caf4cc3957f3`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 4.4 MB (4390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7070061354df3a61218eac1ea2539ff3be9103f86ee0b09e4fb41827e762722`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14d55688805c2e1c614d513ecb4d7f4870837bc8e17163481e6b77a6c96e3b`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd5a17a5c82578f1e7e67d83b1d0490a50d5648a66854ebf956001cc36d7c0`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:4abeddf0514a353212971d22dac3dcd0f362eb5673c5dee566a64a66dd0112f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e928c18ae2b7afcf2dea0e43582ea72f94f386a85415c22902a8b67b189c34`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
USER notary
# Wed, 29 Mar 2023 18:08:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fe6407f813eee3328c3e3f4bbd5ee13b51acde95006059cfb731f7988943bc`  
		Last Modified: Wed, 29 Mar 2023 20:02:06 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb27e6c7f9cb4bd86bcf086d62affd7ae9ff7ddd66d35b1e968864cbd01871e`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b0bd116bf381f3b9b420f35e74669226ff0912664b3b7952bba9201986614`  
		Last Modified: Wed, 29 Mar 2023 20:02:15 GMT  
		Size: 4.6 MB (4575891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7b49dc7a7633c397ab80131dd1867ed00c1370efa343eda4422598ee41df9`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35c4944b89fc1336c998b8f12403111ec969b6da3225128d43e94385d8af41b`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba9413a1ce459d7b222d8aa6ca7717f479471558ba35680a895fa2e0f51c372`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:4d2232090121bf9ac15b6795c48c5cb044ec491cbf2301b1935d12acdcb08108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d39a2949abbafdea0115a7a57686e7dd4916cbd982427a0554c3e1e6ed549b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
USER notary
# Mon, 27 Mar 2023 22:22:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d0b9967527e3e2fe9a387dd1b08ba83b7816d9e3863fb0f3e9c0a13f0225d`  
		Last Modified: Sat, 11 Feb 2023 09:33:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff45c2db506b53371307bdc344c0861a7dd46c067b7093b0e1438a9169763bf2`  
		Last Modified: Tue, 28 Mar 2023 02:19:41 GMT  
		Size: 4.3 MB (4296127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a7745a51f0bb73870d3c3e51184f9e8c17cb255c610686303d779d8e8ae5f3`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7280e5333b6db0e7a4bd1040d64cdd22f0ea2a0be0e5915f04527f9e919b8`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ad4046a4cfcff2ef9ed79f2cf56658913e7388f6452b8e517515c073ce64d7`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:823461cd01b0fd0259a46f88378f2ef26a524180f73e7f7c597ff1a4a0e7d9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da5c2782a47cd55a3bd7cdf3bc6e1bbbf51e781214faf08e95d216dd742e1b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
USER notary
# Wed, 29 Mar 2023 17:42:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496bacdc3e38b8319b094c7cd682983189e795236b61f362a29c0e8e94ceb5`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ac2c8f346280fd047876860be1d522eae075adf2d30efb94fdc4359a6a466`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6285fd241fb1dfa279dda67f86a82bba946327691def1fa78a39f4c89ada4cca`  
		Last Modified: Wed, 29 Mar 2023 19:02:19 GMT  
		Size: 4.6 MB (4605233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6782926d2ef6333a909143ebaefd4b7625218c9d51736220d706c18042e58514`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a74ae17430841be98efe2e7d781cd1e06e782f63bc9e518418223c65faad36`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5dc0e9da342d2163be0a01321aec83eebcd17421d2e45306b09d0b270874ee`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:242b047aad4166071a9fc78cebb537d5cf1b448900a50d3243c35153fec52cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:82e6cd74a4dd40ffa22a7171e7fd0a013e59f87577b37bd82089cc62cf48bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7571272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08054659a657d14063d1a7d6e89021e83b764bba98b922fe7c4d07cfc7535454`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 18:19:28 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 18:19:28 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:19:28 GMT
USER notary
# Wed, 29 Mar 2023 18:19:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0647f7d50bd9007a9af72eec9925f5e3e4e0c35d1796c4a0970fca9f7c127a2a`  
		Last Modified: Wed, 29 Mar 2023 19:31:54 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0616adcfb81a6d2087ac3d3915f5ffdfe33d1df0716cfc8fc50c4060d9cfbfa`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a5272838ec44589c294ff87c9fed67ea835505803f114918c0e9d078c75d6c`  
		Last Modified: Wed, 29 Mar 2023 19:32:03 GMT  
		Size: 4.8 MB (4761329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9029690a2f5060d5204b6e65bbe79c9584edc7f2dd4c0ad30904d9e788c1cb6c`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 89.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da760519592321c41dd788dd127d45f8add2a4af924d0d60c269af2b17fc68`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 347.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c054a9bc9cb6a5f4374f9fc7c2bcdd000d44a564df84e863e7447702fdcbda`  
		Last Modified: Wed, 29 Mar 2023 19:32:02 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:1b859eda30eea52686ca1e25104c8f6c54b7a110e709d1a4f318ea05c4fc28fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8544b97c1f8075ef86c3cd4f54f6e27fde1a0da79ab270f04d28b956cb23bb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8867bd3aa695c936397740852a2a23245f7a8147431da0dea7ea79cb52c3fb7`  
		Last Modified: Wed, 08 Mar 2023 00:17:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46389c4cd7729b78c0a52df7daa142aedd2c1e21f6d97ff7ebd1a32b0936e54`  
		Last Modified: Tue, 28 Mar 2023 00:21:07 GMT  
		Size: 4.5 MB (4524262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7249b0975a56b424c7ef1643a7155c785f29e8785efa46c4d98c1db7be99ef`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4071d49d37fd4ab8f37c67b5104e1db516290ac99a3c7776fdaa98b1a113af66`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52c19763db6fc8e5bce84d899dd56c58e816226c24f2804400fba9ec85ec9a0`  
		Last Modified: Tue, 28 Mar 2023 00:21:06 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:10c586a083e1cf792bb6b0682382049a016d694026a180b33c4c6318518fccd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029d8b16e8f0c4de8efb5bcd1c92443c642a4304b88a248e0b001fb2c565535c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 17:39:20 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 17:39:20 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:39:20 GMT
USER notary
# Wed, 29 Mar 2023 17:39:20 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b02441c89b609b85e27619f8e09f858e27fdac246a198c3e19163753fcb092`  
		Last Modified: Wed, 29 Mar 2023 21:25:30 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dd30044d17dd0900f33ee4cd64e106aa2d710607e560c51ad8bc6fd3172e8e`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f118ec6fe198848420882ff6a719579c9fa2b092eaa7f4aa4ea4caf4cc3957f3`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 4.4 MB (4390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7070061354df3a61218eac1ea2539ff3be9103f86ee0b09e4fb41827e762722`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14d55688805c2e1c614d513ecb4d7f4870837bc8e17163481e6b77a6c96e3b`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cd5a17a5c82578f1e7e67d83b1d0490a50d5648a66854ebf956001cc36d7c0`  
		Last Modified: Wed, 29 Mar 2023 21:25:38 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:4abeddf0514a353212971d22dac3dcd0f362eb5673c5dee566a64a66dd0112f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e928c18ae2b7afcf2dea0e43582ea72f94f386a85415c22902a8b67b189c34`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 18:08:35 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 18:08:35 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 18:08:35 GMT
USER notary
# Wed, 29 Mar 2023 18:08:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 18:08:35 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0fe6407f813eee3328c3e3f4bbd5ee13b51acde95006059cfb731f7988943bc`  
		Last Modified: Wed, 29 Mar 2023 20:02:06 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb27e6c7f9cb4bd86bcf086d62affd7ae9ff7ddd66d35b1e968864cbd01871e`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b0bd116bf381f3b9b420f35e74669226ff0912664b3b7952bba9201986614`  
		Last Modified: Wed, 29 Mar 2023 20:02:15 GMT  
		Size: 4.6 MB (4575891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7b49dc7a7633c397ab80131dd1867ed00c1370efa343eda4422598ee41df9`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35c4944b89fc1336c998b8f12403111ec969b6da3225128d43e94385d8af41b`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 350.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba9413a1ce459d7b222d8aa6ca7717f479471558ba35680a895fa2e0f51c372`  
		Last Modified: Wed, 29 Mar 2023 20:02:14 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:4d2232090121bf9ac15b6795c48c5cb044ec491cbf2301b1935d12acdcb08108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d39a2949abbafdea0115a7a57686e7dd4916cbd982427a0554c3e1e6ed549b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[4444/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
EXPOSE map[7899/tcp:{}]
# Mon, 27 Mar 2023 22:22:31 GMT
ENV INSTALLDIR=/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
WORKDIR /notary/signer
# Mon, 27 Mar 2023 22:22:31 GMT
COPY /notary-signer ./ # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
RUN ./notary-signer --version # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./signer-config.json . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:22:31 GMT
USER notary
# Mon, 27 Mar 2023 22:22:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:22:31 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d0b9967527e3e2fe9a387dd1b08ba83b7816d9e3863fb0f3e9c0a13f0225d`  
		Last Modified: Sat, 11 Feb 2023 09:33:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff45c2db506b53371307bdc344c0861a7dd46c067b7093b0e1438a9169763bf2`  
		Last Modified: Tue, 28 Mar 2023 02:19:41 GMT  
		Size: 4.3 MB (4296127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a7745a51f0bb73870d3c3e51184f9e8c17cb255c610686303d779d8e8ae5f3`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7280e5333b6db0e7a4bd1040d64cdd22f0ea2a0be0e5915f04527f9e919b8`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ad4046a4cfcff2ef9ed79f2cf56658913e7388f6452b8e517515c073ce64d7`  
		Last Modified: Tue, 28 Mar 2023 02:19:40 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:823461cd01b0fd0259a46f88378f2ef26a524180f73e7f7c597ff1a4a0e7d9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da5c2782a47cd55a3bd7cdf3bc6e1bbbf51e781214faf08e95d216dd742e1b3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[4444/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
EXPOSE map[7899/tcp:{}]
# Wed, 29 Mar 2023 17:42:02 GMT
ENV INSTALLDIR=/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
WORKDIR /notary/signer
# Wed, 29 Mar 2023 17:42:02 GMT
COPY /notary-signer ./ # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
RUN ./notary-signer --version # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./signer-config.json . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 29 Mar 2023 17:42:02 GMT
USER notary
# Wed, 29 Mar 2023 17:42:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496bacdc3e38b8319b094c7cd682983189e795236b61f362a29c0e8e94ceb5`  
		Last Modified: Wed, 29 Mar 2023 19:02:13 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ac2c8f346280fd047876860be1d522eae075adf2d30efb94fdc4359a6a466`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6285fd241fb1dfa279dda67f86a82bba946327691def1fa78a39f4c89ada4cca`  
		Last Modified: Wed, 29 Mar 2023 19:02:19 GMT  
		Size: 4.6 MB (4605233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6782926d2ef6333a909143ebaefd4b7625218c9d51736220d706c18042e58514`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a74ae17430841be98efe2e7d781cd1e06e782f63bc9e518418223c65faad36`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 348.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5dc0e9da342d2163be0a01321aec83eebcd17421d2e45306b09d0b270874ee`  
		Last Modified: Wed, 29 Mar 2023 19:02:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
