## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4ff028c21eb3f48f6964d6b2293993981ea0cebd934aa83cdda897d3120224f9
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

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

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6ecba94a9cf59da2afe6378b397ed843b4b262cdb7ba65ab3b93faa76b2177e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235660175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8579f466b8724636b9c8202c28b0db1092a5be242387b549f5c2e4f78b03ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
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
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d2c314d35b9605a5c7a3e3a16f57671383b7401f7fdf30bfc007dc15255c24`  
		Last Modified: Tue, 21 Oct 2025 16:20:25 GMT  
		Size: 91.6 MB (91601698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cda0fab2aaf129da739863007a2fecaf7cb405228b77e5f8db73c1a9fa7680`  
		Last Modified: Tue, 21 Oct 2025 16:26:54 GMT  
		Size: 90.9 MB (90947957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8ddce0fde5d776f3a4f1f1aefe33543815ec078e2ca0443bd28fa1c552ad98`  
		Last Modified: Tue, 21 Oct 2025 17:14:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0482e6fbd7730ad6b68cb37cf3809851f898568f09002fe10c2bd2c4c553c2`  
		Last Modified: Tue, 21 Oct 2025 17:14:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b3d4971d09fbbab1de70e918116b368e71db5295aae94b189e834625c295a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670d1b60150064f5e57c33c1191024cc5fe2e2641f5100e9576e4da36862ea04`

```dockerfile
```

-	Layers:
	-	`sha256:9b0ca2dbbfb19f17dd04a2d6b0a6b9dfa982018e1bd2572d0d2c72bd7e6bb022`  
		Last Modified: Tue, 21 Oct 2025 18:41:29 GMT  
		Size: 7.4 MB (7423946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938bbd41c8c992a2d396ecbc4a51a1441475a43dec3e62f303d0c55eaebe7b2b`  
		Last Modified: Tue, 21 Oct 2025 18:41:30 GMT  
		Size: 16.5 KB (16516 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

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

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:91c10f7fe9f20b9e43c5b7ab258b3b48f5d5607d4a11ad4bec7ccc375e137d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224066192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7398996119884975d21ed77a22653a5b7e49d44ecd978ce790e2fde7098fbfb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
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
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca86749dd1b3672cc7f1733b6e5f5372ad093de9579102315cdb11ae045544`  
		Last Modified: Tue, 21 Oct 2025 22:43:42 GMT  
		Size: 88.2 MB (88206454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a849a5fcb0797c11fd34bbef23e7b62d65a3247bbd6c6e09633d667f0e10958`  
		Last Modified: Tue, 21 Oct 2025 22:48:20 GMT  
		Size: 86.5 MB (86506996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0189bf6dcdd22bce00af0f6fb1be0ff35449a3ae9eea91381d3f3ebcf93014c5`  
		Last Modified: Tue, 21 Oct 2025 22:48:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66887a4980cb484cbcee410bbae7b18321927167b6e9939fd28aab5f06146866`  
		Last Modified: Tue, 21 Oct 2025 22:48:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a99096d4f5fab1ee8d35628997ed8e22fc091ac792b1cc1d57db49eb6192dee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf5a6001d1a0707582b053a41523f762031491820e9c78281767537d8f9b14`

```dockerfile
```

-	Layers:
	-	`sha256:1df87dcd6b0ab00ae0449a653b3bc7bfe7bbb92fa1490a1d779d26dbb99afc94`  
		Last Modified: Wed, 22 Oct 2025 00:41:22 GMT  
		Size: 7.4 MB (7416687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a6c91d96c23725337fb903ce0a7bc6c4313ecc5a8af5409740e9582a505bac`  
		Last Modified: Wed, 22 Oct 2025 00:41:23 GMT  
		Size: 16.5 KB (16458 bytes)  
		MIME: application/vnd.in-toto+json
