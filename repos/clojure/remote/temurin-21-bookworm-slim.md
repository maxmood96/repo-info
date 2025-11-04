## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:68f2ee443507ac093b616d351239ed1295a992897b097efa2810b67ee27dccfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f263b2b243e2d3db6961e84434e1d49668a897b5befb68ae837bc781087f8ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255713817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee2ba3bc4bb29d4fe2fdc5c19f4190205d65a471b35c14bf2e98ad97176d85b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:42 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7734c83a371733bb864682cd8d5d039e9fe3f1b2be0a2e7ca7d68a203d6f8111`  
		Last Modified: Tue, 04 Nov 2025 10:54:15 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e60b9956640fa3089b1f288f50f34a23d20dcbf621f7e42685a0c7c09f3e7e`  
		Last Modified: Tue, 04 Nov 2025 00:56:38 GMT  
		Size: 69.7 MB (69679469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7002656dbd8c51cca7ffe420a07c774e8e0550ea65a84cedbd2330066ba2ae`  
		Last Modified: Tue, 04 Nov 2025 00:56:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f713f88fc2f385b0f511945ded1d5eccd14f2ac0055956c1ddbd5a6ec0ea93f`  
		Last Modified: Tue, 04 Nov 2025 00:56:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ad260177a1192cf68d4570018b50c1bcdd3ee2056505793beaa74d9dd9b95bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520bba91dc1e4e7d28e2eef0c587f1d1bbb76865714a7dcb41bc15142068cd9b`

```dockerfile
```

-	Layers:
	-	`sha256:0c83d9880e010e0fcc5e1fb9eb40f8279c27f45384c63e93806ec0f175934b01`  
		Last Modified: Tue, 04 Nov 2025 10:42:24 GMT  
		Size: 5.1 MB (5116490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691721b49462440535ea1633d8116d8bf9476f5acac641b1afe1bcdf3afea6ef`  
		Last Modified: Tue, 04 Nov 2025 10:42:25 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2992d2f4c04e806dc4bf95bb6a9f75b70f2fdba586918b58bee5fcc774df1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253745042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76aa30c8930d1c43e34b245946ead0a4d84d9f30e21a0d0bfa110d8050b8706d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:39 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf94c41977d44e71a396dc15492143705666ec5c507fa77658d8d27e40bbb15`  
		Last Modified: Tue, 04 Nov 2025 11:08:50 GMT  
		Size: 156.1 MB (156081254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f5cde205bdd2a442a163030c0b7db400cacf7a865714fe9798d5af8d6240a9`  
		Last Modified: Tue, 04 Nov 2025 00:57:36 GMT  
		Size: 69.6 MB (69560370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0571278ad1a4acb375eb5d8017cd862ac1de98cd556d34087f2a713d36562d`  
		Last Modified: Tue, 04 Nov 2025 00:57:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d2bb55f5c5bdbfe578d0cac91a954c830eafd3a954d1e8f46ac2265efe6e19`  
		Last Modified: Tue, 04 Nov 2025 00:57:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74cd7daf4c5fe2d3faf927c768782d5265f096b2305b4847dafcb9d1eb5e140e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36659d01f3a6af5d8b91be0bb650dae61db093307d6eb6f498e77159007a86d1`

```dockerfile
```

-	Layers:
	-	`sha256:c8301284d98f3d58d2c221df426e21ac524ccd8afd3e9f51fe7a0b98e81ce150`  
		Last Modified: Tue, 04 Nov 2025 10:42:30 GMT  
		Size: 5.1 MB (5122251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e73b3c4c6860f218d4b4c6f753c4e006b9892ee2805e26d54fc0605cac4de2`  
		Last Modified: Tue, 04 Nov 2025 10:42:30 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:75151f156f9037ff03db7db66670fd3bba274e5a56119aaddf2c2d2af637e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265546108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef5275c5168cdcfe4109b28b44c131b6da1329c84b390dc2370db8bb41ebb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4de39d3ceb05c0fff8b1118b58bf5502c7dbd9415c253b8957509f09667345`  
		Last Modified: Sat, 25 Oct 2025 01:34:32 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5006614cf14880b72d679c4c58910d5e4758f69588a2bb01b6b1d1fe0ca48`  
		Last Modified: Tue, 21 Oct 2025 16:12:25 GMT  
		Size: 75.5 MB (75512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2a48bd0b7b53c0183aa67b5b6f32bbb67cb6a299726a0026b9fad9ec2fdcc7`  
		Last Modified: Tue, 21 Oct 2025 16:12:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b161f9ef0ce91b026a24c7c3a96e0ecf17858c000b50b5984f35eed3721d8`  
		Last Modified: Tue, 21 Oct 2025 16:12:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fe3e335314fdda39a046109db5ed766ea64fc12bd3774ac544099db369959da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2589e6ec1122eacd73549feeecef76ff7af84e21babd0240c18cf3b93fa87d51`

```dockerfile
```

-	Layers:
	-	`sha256:af193f691da4a3489888785d5a332e2c35d99e219947158e8fbc180b16729740`  
		Last Modified: Tue, 21 Oct 2025 18:38:36 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797b5f69ee6cf262c06469c875b484ceab97b69a1fc8164c2aa27ac1aaf85606`  
		Last Modified: Tue, 21 Oct 2025 18:38:37 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:952f7a910824c4278f4d5be242ec7655b6b16bfe99c6868e87419fb3885234f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242403160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28e4940fdd680059996610c3be1e35ed07480532ea9d27d0282a700090f3922`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:30:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:30:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:30:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:30:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:30:45 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:33:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:33:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:33:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:33:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:33:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a451f1a4798f1ccc1846aeb760a08a1d0421d96b1dcacf9ec3aee8907e026048`  
		Last Modified: Tue, 04 Nov 2025 11:09:26 GMT  
		Size: 147.0 MB (147027017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3da6cafc4cc0ca2777930199edbaabeff71f2b1d4860fc5a63b5a8168b1a766`  
		Last Modified: Tue, 04 Nov 2025 06:33:38 GMT  
		Size: 68.5 MB (68490552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22e7519e148848954fc1a879927fb97dbac0aceb31b341cd7628ce7794e33e2`  
		Last Modified: Tue, 04 Nov 2025 06:33:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8737ca6957ae7636d9071e8c857117dcb3226b39a07a9ee7fcd5d385f58727`  
		Last Modified: Tue, 04 Nov 2025 06:33:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b85ae7bfda951fbca5d206d2e58fe03d46fc0e1d64cd4bcf6eb84219f4b7c946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cf22553c568ebbb50e2934ff75d3360cbd5986e0ec81bc61bc0005e3dc50b7`

```dockerfile
```

-	Layers:
	-	`sha256:915fee468bb2f9d91a607e382e884e4ceb5383dd5f0240820848751c876a487a`  
		Last Modified: Tue, 04 Nov 2025 10:42:39 GMT  
		Size: 5.1 MB (5107811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc9bab155a08b5a6b5c37ef7f33e6cca1f4063fa11c8f7f982fab5927214300`  
		Last Modified: Tue, 04 Nov 2025 10:42:40 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
