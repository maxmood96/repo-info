## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:c0575cd7accb4828320ed988ec5f3e20853e7157a01a18ae1883712a9fbd8f34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:354eebf1e846b10b27c9b41e2e538a717862540ce4e501832c13a0a1941e0726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226864186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3658abe0b3c8e811c5b32e9cf851e1b9c1ec66b8038a677032394f448c2e53d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f40155553245673953e2d6f7a1d1673726b4930a750c5fafc69aacdcda00d1d`  
		Last Modified: Tue, 21 Oct 2025 02:24:58 GMT  
		Size: 92.0 MB (92036044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae868f9b977a492aebdaa61578e144f62e547413be45354b9bc8b777a3074bec`  
		Last Modified: Tue, 21 Oct 2025 02:24:53 GMT  
		Size: 85.5 MB (85542129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b0ef158b2e44de3eaea1ec4e58749a8789acbe433745ed22cdd8067c4a8e7f`  
		Last Modified: Tue, 21 Oct 2025 02:24:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495a6d936d467378f444dd8678d7dc917d97503b62551c86eee901d1c8f8cf8`  
		Last Modified: Tue, 21 Oct 2025 02:24:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b2c3fe20b954d06e7b1dab3feac5d4b00bf024f11b9cc627739c1bbd76d80088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338c0791a1bde0c74ea0bb1db68363026eaa66f7bb2f4d160832f7db51f4d248`

```dockerfile
```

-	Layers:
	-	`sha256:0b46cae8a1d5259527628b7924b4d65c08205a4723efed27188947d4d6412bff`  
		Last Modified: Tue, 21 Oct 2025 09:45:28 GMT  
		Size: 7.4 MB (7418217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0d00767a9751163417ee75136f72cefa12b204a97037ca84b5584387b1a010`  
		Last Modified: Tue, 21 Oct 2025 09:45:29 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bed230fc02d0068d15678b91c6b83b5a3d9606b1ff5d76c83e42d52b5fc324c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226058747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89c0159c6eab78bdcd992445eeba66915c5cfa0d4690db671db263b020a234c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7dffcb1a39357d1597dbadaaa0d08bf7fe9e468b6e4698778068bb5ec47ba9`  
		Last Modified: Tue, 21 Oct 2025 02:30:32 GMT  
		Size: 91.0 MB (91045255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30b1b1c735d52ed8d59b2e2cca362425c9f04e5f793719b8840344d8b693c43`  
		Last Modified: Tue, 21 Oct 2025 02:30:31 GMT  
		Size: 85.4 MB (85362706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c7402e3889140e34e7f0934d6d249f79313cf73e87a1d1f5ec09595d53c4f4`  
		Last Modified: Tue, 21 Oct 2025 02:30:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b54afc63186ca07dbe520a8b7e79163b587b94c9e18dc567127909e4984fff`  
		Last Modified: Tue, 21 Oct 2025 02:30:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d0f0e2f02b20793898e9bb49a68e471f2aee9a7c27406ce7c37032ab788cad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416056bff43e737faed7d40ef5a4c738b2a7287a3c31cee4eca2468c3fd30f6d`

```dockerfile
```

-	Layers:
	-	`sha256:a3c88e4b5355f2f4eb8ea24124b68424304f233b172c589491ffa503842499f0`  
		Last Modified: Tue, 21 Oct 2025 09:45:34 GMT  
		Size: 7.4 MB (7425268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade1eb3db35363d4eb91a695899217b591f1756036c529e49dabc949a11dd1de`  
		Last Modified: Tue, 21 Oct 2025 09:45:35 GMT  
		Size: 16.6 KB (16599 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5efd5041829966189195fbd96d447d852fd191e46fb9c1220f80d9e7a0929e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238863400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9617a83bcd8623ca7f5b108425b65c7f03ca031ec62f05ed76156eb3a4f49b8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc92fde2234dc8f32a119fed41daaf6c83b22fa10ffcee1fa59c6b6dee4280b`  
		Last Modified: Fri, 10 Oct 2025 05:55:27 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b43cc112095259207d0322906d05bfcc97f724ef14f1fbad24b57739c2e44d`  
		Last Modified: Fri, 10 Oct 2025 06:05:08 GMT  
		Size: 94.2 MB (94151423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e543c8514e99e2f6002ad39b0c3d0162a03d604fcb416b8dc0fc7fa4490799e`  
		Last Modified: Fri, 10 Oct 2025 06:05:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920e4968a8c1f3a2cf04f5f81e2dcd54633ac72ac8a3876a79334953774a4298`  
		Last Modified: Fri, 10 Oct 2025 06:05:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d4867dc79a1e99b4053ff50937b51027b25764f7e69b29fa27e9c71c23a39024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eb3188376f38cd2865d16f72d8f8ed516ee5f2e59981d102a12befa6c3ab41`

```dockerfile
```

-	Layers:
	-	`sha256:5b20e324ef4faa74061b5746dc3089f7e8ae7b8d72b0f77a5c866a5ecb0026b4`  
		Last Modified: Fri, 10 Oct 2025 06:49:20 GMT  
		Size: 7.4 MB (7423946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff50ff0d6f8195e14e74a05b14260054782a9cf8922697d7adc1c80a001c9756`  
		Last Modified: Fri, 10 Oct 2025 06:49:21 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:aeb419c1621b4ef8f57f41825532dfe0a52b962ff1b0555675557a1dc611851e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225572783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedde76c13dd9eef7ff2cb1c762d2c5f260bf5c3e259b1b1654326796557be79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15c689286839ede10d92025dec031597f1addd346fcb57828df1d0a46794634`  
		Last Modified: Thu, 16 Oct 2025 08:52:21 GMT  
		Size: 90.8 MB (90752401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d0d2e36f71b92109dd136c1dbbe64e201bb1e81adbfde559e83108d077a7d3`  
		Last Modified: Thu, 16 Oct 2025 09:12:25 GMT  
		Size: 87.0 MB (87049331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3be30d12f9d52a7c000ee469322eaf37b0b6f93a2ac1ffc16845a2e50c6896`  
		Last Modified: Thu, 16 Oct 2025 09:12:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808f49f96d50526223874f5ae60524e0e312e970fe22ec1922de1b57f3588ce5`  
		Last Modified: Thu, 16 Oct 2025 09:12:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e920867f0f7bbfaacaac39d3093a56add268cf794a6b0484d3636eb68462e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52d188f5a2140366f5c914cd9d020e64726e9d4e5ba199e34bd93f5726e4309`

```dockerfile
```

-	Layers:
	-	`sha256:0cd00e42cf41e0a41ce5345a8111d252948717f996f951d87f3e82ff409ffa11`  
		Last Modified: Thu, 16 Oct 2025 12:36:47 GMT  
		Size: 7.4 MB (7406139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd072e33a67610fdf7a28bc10869bacd48882f0a8db6096a1d671125c5c36b28`  
		Last Modified: Thu, 16 Oct 2025 12:36:48 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:289b9a776834cb9868f225c36ac5fed6e848bca03f3917b95d3431568df6093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226684063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6544e1f002257467650a58f2d87759c3f99f4c86fef152c39b03edb239a83d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c472da08548dcf037f943b616dabad9bb86cbf698dd3af1da4c39e1dc1031b7`  
		Last Modified: Fri, 10 Oct 2025 03:42:21 GMT  
		Size: 88.2 MB (88206430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83036269757bedca8ae87dd13c2e369618f3fd2ed1867c4958e70ab146d3a731`  
		Last Modified: Thu, 09 Oct 2025 23:51:45 GMT  
		Size: 89.1 MB (89125151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2c9bb8ee0994b08fec82d5fbc151fcfaee47f86b8ab918be05f68ff13a77c`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97803e1302231335318fcff0bbf952ab0ffb5a47aeb4b57a7b0d160df90f47a8`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e6bbf66a2756b999f26e03aa58fa780c302eb5e528b4b36c310727092ccdc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5228de3b5a12804321d7b7b2a9357aa6e0ba2b3243436fd2c3a12cff3c2384`

```dockerfile
```

-	Layers:
	-	`sha256:83d959366a289e23ced4883c34cc95d6d9c817733a188c0b3df7ab93e04371b9`  
		Last Modified: Fri, 10 Oct 2025 00:40:48 GMT  
		Size: 7.4 MB (7416687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2971deeffbbe67e7927f6cc8b7743c1d0699c305a431237d94a28079d7c7e236`  
		Last Modified: Fri, 10 Oct 2025 00:40:50 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
