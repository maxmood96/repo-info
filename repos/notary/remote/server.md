## `notary:server`

```console
$ docker pull notary@sha256:83704113a443a653ab47f39dc9a53e8251d5d69f7846fec3e76690495f2eb476
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
$ docker pull notary@sha256:c25acc281cc4dba7845a6833e6594f43ef5883702d8c1698f02fa3e716a49bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366330a90ca821500766354fe230c518062d59a5403a28ffbfef7eed86e29753`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:45:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:45:31 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:45:31 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:45:31 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:45:31 GMT
USER notary
# Mon, 27 Mar 2023 22:45:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:45:31 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b9e3dceb52b5f1909f74e5761d8b0968630630d4c5d37134133ff1529d57ca`  
		Last Modified: Sat, 11 Feb 2023 02:02:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9362a2b1100a2d3d12c1fa9941ef61cde36540c7d918725c75f1730eaaed51e`  
		Last Modified: Sat, 11 Feb 2023 02:02:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a28dc88849079870b9e4959d4fd032d12faf28661eb350a7be93bb2e9fc0ed`  
		Last Modified: Tue, 28 Mar 2023 02:21:47 GMT  
		Size: 4.7 MB (4732810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2b52873920b7c98577e11142a92cbc5838b485f997dfba1b850500f4c14000`  
		Last Modified: Tue, 28 Mar 2023 02:21:47 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c71ed38e49fc386b13f8cad2ba46b5449d12ba67096acbe0c7ca2a4b53d3838`  
		Last Modified: Tue, 28 Mar 2023 02:21:46 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff8ac18890cb01482ed1d364ecf5103c105bbda6fed2ab06543fd0d77a6a765`  
		Last Modified: Tue, 28 Mar 2023 02:21:47 GMT  
		Size: 384.0 B  
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
