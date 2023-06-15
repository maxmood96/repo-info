## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:dd325acc84c6c058425b10c0d26b6324041a01f8c35af50902d8ce0f235c6971
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
$ docker pull notary@sha256:5f504b471d38be091610f65c97bf8e5a283e8e7e91ba21555b391795d1dacb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558e66ffd6d39802f3a23ee60cfb0cb80922eb393779dd6f36f3888c17a79a44`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:45:51 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:45:51 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:45:51 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:45:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:45:51 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:45:51 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:45:51 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:45:51 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:45:51 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:45:51 GMT
USER notary
# Tue, 02 May 2023 18:45:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:45:51 GMT
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
	-	`sha256:a223a56405ec28642db9bbcde4b5bb773b94d7d3b84480d7e487417c84658e14`  
		Last Modified: Tue, 02 May 2023 20:11:05 GMT  
		Size: 5.1 MB (5147824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58867ebec3bd184ec604e217a61d14918e4b611c6160c15a59d9518aec1d2290`  
		Last Modified: Tue, 02 May 2023 20:11:04 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793af072346077ee23aeefa900ad9e9946777058e7adca0346350c815a0112`  
		Last Modified: Tue, 02 May 2023 20:11:04 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626c70d5d7fd7a1d7d46fbac03b4a97b143b913d4b48827adf6267363cb7b0e2`  
		Last Modified: Tue, 02 May 2023 20:11:04 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:449c89eee37b082013c6846cc531711c3e4e2d77a7ad7e0d136da30bc7ff0767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f389c9336e8801ef6cd83cab750eb3363c7dee34086865188f949ddd4b0883f7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:28 GMT
ADD file:41a85835978e4acba9d92833f0d5e20084da50779e52d8832d576b003a7aa1bb in / 
# Wed, 14 Jun 2023 18:49:29 GMT
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
	-	`sha256:053f9b31dd2e619ba14dc3733515fcd65e92851f612b94453db88ea1d27ab0ea`  
		Last Modified: Wed, 14 Jun 2023 18:50:10 GMT  
		Size: 2.6 MB (2615570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8b1ea8ec24955304373c42ddad13462ec8177200b715cdae1220f4372b27ae`  
		Last Modified: Thu, 15 Jun 2023 00:03:34 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d8bfd5064c36b13e7990e5b4d4034b9248ab5e803f32073ba3dec6ee678899`  
		Last Modified: Thu, 15 Jun 2023 00:03:32 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4735db51b68a16da59724f275087f706e1dc85f98b756e77012beb7e7f1c7`  
		Last Modified: Thu, 15 Jun 2023 00:03:33 GMT  
		Size: 4.9 MB (4893576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1544046379bafd9f16c386e348572696174a7e5de3d39cb1dbe0513f4c2590d`  
		Last Modified: Thu, 15 Jun 2023 00:03:32 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0afcf911966e6028390980e4519af147da9b40f87540a11229bfa15618e2fad`  
		Last Modified: Thu, 15 Jun 2023 00:03:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8225d1b24b673d04afdf4f3d8affeb8bbaaffd894f9b119a035c3145c40930eb`  
		Last Modified: Thu, 15 Jun 2023 00:03:32 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:e477b0c3162ca645b8aeac5983bb96f5cd95e9617c66ee23a190b9e3626dea89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988ebdf8bae58a74eddc8ed4986a4ab9e74884ed8a0de07a7060a93e7f7e73c3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
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
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4a70fe37c8d33b219ba725d1903a536b2d54bd47305e1c9d9a969b379ece36`  
		Last Modified: Thu, 15 Jun 2023 03:04:58 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a034e17957ae3c49bb611a8be82f0a3471bf7c65d72c9a3222f117b057f486`  
		Last Modified: Thu, 15 Jun 2023 03:04:56 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a624c4a09b1e59b84d684f8415dcdf778395842b4feb9b5cf5417203e2ceef`  
		Last Modified: Thu, 15 Jun 2023 03:04:57 GMT  
		Size: 4.7 MB (4734457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593363fb96cc338299b1dfada96ecd19bb7cc3768d1247ebfe8ccf8dcac7e9bb`  
		Last Modified: Thu, 15 Jun 2023 03:04:57 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9b840c78778ec16ae9c0775d99005e75fb2be7e630f8c52b4bf59c4fa1271`  
		Last Modified: Thu, 15 Jun 2023 03:04:56 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f92033697d8ecc6b52f80f9f56c2f981021c9949fca2c8c5f934f7479b8c4a`  
		Last Modified: Thu, 15 Jun 2023 03:04:56 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:68393a4e185d139e358c8dfaa97ffcbaa667fcd0ff45647de4203f3eda3ab97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935cb249bf13bc3961d21f81e31ed017e69da2e0ed7cea17839ccf1353c86776`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:50:10 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:50:10 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:50:10 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:50:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:50:10 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:50:10 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:50:10 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:50:10 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:50:10 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:50:10 GMT
USER notary
# Tue, 02 May 2023 18:50:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:50:10 GMT
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
	-	`sha256:4f80ad87e3774805092bb5683294c6a76355af6830865e0ac78b13fb860ef24d`  
		Last Modified: Tue, 02 May 2023 19:10:50 GMT  
		Size: 5.0 MB (4950778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3f11638dfa02e7297a61f22a6672d00f03712f5b945084f22cbe7a9dce42bf`  
		Last Modified: Tue, 02 May 2023 19:10:49 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cba988801087fc69387af6c351dab4779ee3ba548f3e874de04a5a1002863e`  
		Last Modified: Tue, 02 May 2023 19:10:49 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cd63622d83cdbc333d9ed47700522ce7a12408cf6728792112599827cce254`  
		Last Modified: Tue, 02 May 2023 19:10:49 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:995dcdf8f9c15a4a963963fad1d6042b8ad0e06deb28b75ecf775c24399eef57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7446064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d9a3e9aea1dd1df8ab6b019d016b59fe2fecd1e65653682819b9898e48fd1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:59:30 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:59:30 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:59:30 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:59:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:59:30 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:59:30 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:59:30 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:59:30 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:59:30 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:59:30 GMT
USER notary
# Tue, 02 May 2023 18:59:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:59:30 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eea900e54ccdc885e48cf524add82df276a804af096abc866a2cb00078bf29c`  
		Last Modified: Wed, 29 Mar 2023 22:35:43 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dfa1fb665cef120a2e530d1a24146e1b9c7bbb8b713371641a879d2fa14d0c`  
		Last Modified: Wed, 29 Mar 2023 22:35:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec548c148335efb5453a17cc8d52545e486b867cae158b89083b00eb0203ddfb`  
		Last Modified: Tue, 02 May 2023 19:21:01 GMT  
		Size: 4.6 MB (4639159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4045ae21ea722ca350703b16b17124683d99800f35cc75fdded0ca83275dfc`  
		Last Modified: Tue, 02 May 2023 19:21:00 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab81832d11ffb94780846be158da2eb98981eb44ca40f7f78576e41bc71c6c`  
		Last Modified: Tue, 02 May 2023 19:21:00 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405f96efaca407897452c1ad302aa1eea404e65957b6b1c755cbdcab9d1961fb`  
		Last Modified: Tue, 02 May 2023 19:21:00 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:46222102af49c089bdd985dc3a9c9e396e4132f7472daf8bbc8c0948eaaedde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc73865af693435b5f688b2cefee44b2d4bf02679a776101a457ed1d85949b8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:45:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:45:37 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:45:37 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:45:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:45:37 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:45:37 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:45:37 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:45:37 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:45:37 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:45:37 GMT
USER notary
# Tue, 02 May 2023 18:45:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:45:37 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d718f433f226a10233b1c2fd202d613455bab7210ecab0e649f578786e27cc7`  
		Last Modified: Tue, 02 May 2023 19:14:49 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be685ead59433921acfa36285b0d513c970b7e82ab7594887f7bdd7ae37527`  
		Last Modified: Tue, 02 May 2023 19:14:48 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ab63e1bbe686eb9921ae2cc757a2f3a08a4f9ca3ff21a92c5e585ff02419a8`  
		Last Modified: Tue, 02 May 2023 19:14:49 GMT  
		Size: 5.0 MB (4976490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c85d7ee22e60d478fbf8ea9d90ea62a303179efb20bdc85955876a100ffb6b`  
		Last Modified: Tue, 02 May 2023 19:14:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c832954401746d66fbcb12d064382b41ae4fec14f65e876b184628387f802604`  
		Last Modified: Tue, 02 May 2023 19:14:48 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb44149a8d8cccb958cf42b938950bc2199a6db43ff94dd7a1f10585d896467`  
		Last Modified: Tue, 02 May 2023 19:14:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
