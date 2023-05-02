## `notary:server`

```console
$ docker pull notary@sha256:6bcc26670cd3c55e165baa32b29312e13ceb0bf3165cc168149e0169628cf41d
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

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:a8201173483cb211c24326512f4d6e298acf64694ce15c3562fa5bba50d200e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c360688283460f13221fb5dae30dc3548b7601f884caebabc4d27ca1babcfda6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:45:24 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:45:24 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:45:24 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:45:24 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:45:24 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:45:24 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:45:24 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:45:24 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:45:24 GMT
USER notary
# Tue, 02 May 2023 18:45:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:45:24 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68b2bcff70e852a0b418fc8919bf42378c7436f1c4e527b11979889457abb98`  
		Last Modified: Thu, 30 Mar 2023 01:14:16 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab11cf2ddb415363607d7a44c9acca8d79c797b1ba474fc880f2009dce5575ba`  
		Last Modified: Sat, 08 Apr 2023 00:16:31 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78a134c6cc7ea37b2ec046af3175a8cf2387f0977ce0d7bba8f869b7d259781`  
		Last Modified: Tue, 02 May 2023 19:08:03 GMT  
		Size: 4.9 MB (4893575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351534d2c473ad7169471a1c314fa6b5137336e797f74f151cc280b7205a6ba4`  
		Last Modified: Tue, 02 May 2023 19:08:02 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f01fa126d14c1e87100b581d4cfde9dd96bd7af615f780f854529dbf5f1f37`  
		Last Modified: Tue, 02 May 2023 19:08:02 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22ef035e28e63c590c8f53395e52b224c38a95e7aeea0d7000cf2e155a595aa`  
		Last Modified: Tue, 02 May 2023 19:08:02 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:c0fe8f86a82109adf07fa6fd8392d6e0528b2f65301f2760542e75c106225355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7446034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d30e6390aef29234b3679856f76e475db4f96f9e586149dd8b36eec3fc0a736`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Tue, 02 May 2023 18:42:31 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 02 May 2023 18:42:31 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 02 May 2023 18:42:31 GMT
ENV INSTALLDIR=/notary/server
# Tue, 02 May 2023 18:42:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 02 May 2023 18:42:31 GMT
WORKDIR /notary/server
# Tue, 02 May 2023 18:42:31 GMT
COPY /notary-server ./ # buildkit
# Tue, 02 May 2023 18:42:31 GMT
RUN ./notary-server --version # buildkit
# Tue, 02 May 2023 18:42:31 GMT
COPY ./server-config.json . # buildkit
# Tue, 02 May 2023 18:42:31 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 02 May 2023 18:42:31 GMT
USER notary
# Tue, 02 May 2023 18:42:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 May 2023 18:42:31 GMT
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
	-	`sha256:f12b78d6a3e22d73bcaa74138a0b02b19db0b0f9292ba54b601449b2a1abb0d5`  
		Last Modified: Tue, 02 May 2023 20:02:40 GMT  
		Size: 4.7 MB (4734456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384d59ecbabfb78a8dd003b114c3710a03ac83f56f4a43ca8b5f68f4cdd17bb4`  
		Last Modified: Tue, 02 May 2023 20:02:39 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b41c8d5e5fa4bc4bf6f12921787c7bdce36d9c7b1d2079036cc3280851795`  
		Last Modified: Tue, 02 May 2023 20:02:39 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20ba973a380ae0b98d7bdd92c6ea9744ec7ceff3369a9204b59ce63d5c50862`  
		Last Modified: Tue, 02 May 2023 20:02:39 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

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

### `notary:server` - linux; ppc64le

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

### `notary:server` - linux; s390x

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
