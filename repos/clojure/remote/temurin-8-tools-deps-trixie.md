## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:dc3529fd259f0b697916ebaa7316d176f34927e20428387b7b3562330d22510b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:0f16b7bea0f7d8116357c97c27b8d0c986ce724649c69e8b174620248e6c895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189544949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ef3bf4491af70488c310e2e612c3a8e00cd0bdde6ed6209120811d1fef4e66`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef803a75d962c061c61987e1725f204230ef89073578a51d62825ee7f6e6da88`  
		Last Modified: Tue, 09 Sep 2025 12:39:35 GMT  
		Size: 54.7 MB (54731285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778ef37258489f25db42c77299e4afa6406e666de535aa8e62725cea8284aa5`  
		Last Modified: Tue, 09 Sep 2025 12:39:36 GMT  
		Size: 85.5 MB (85533490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d371f06e09d7312f93134eeed36a2948583488dc2d73db5628d5130757e630`  
		Last Modified: Mon, 08 Sep 2025 22:25:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c8a9030ca95090a16d6f2aaea3aea2661ec15ccfc98da30a6ef84ed874013c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e972f4d634c7f6ede39d6252373655e2071d3d6ec1e3f69d378d0ffcd6c88c16`

```dockerfile
```

-	Layers:
	-	`sha256:94982e0d20a3d2f05fe62bf130aae894f6b17325b926411da4475712afbe7bc0`  
		Last Modified: Tue, 09 Sep 2025 00:46:59 GMT  
		Size: 7.6 MB (7588455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386267d53ca9e32d28cae84394efbb375ae6ceb6a98c096e5d88a7648221cd7b`  
		Last Modified: Tue, 09 Sep 2025 00:47:00 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4e0ed7596b62faab0dac31bb6f47f1da76c67f026181b9d23362c41a053df11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188838075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcf3060b51f3a2b149bf24349b020d9fa8f4b357caea511840982ecb42076bf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b495718cf34a8315e886d2826b0155e4e1b3acf18df6867f36be7205d531265`  
		Last Modified: Thu, 11 Sep 2025 10:54:24 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7ef638a256d40cbace11f90b41db8eb262f0ec9c45c6c348d06d73644df42f`  
		Last Modified: Thu, 11 Sep 2025 10:54:27 GMT  
		Size: 85.4 MB (85358078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d97f1dcd0eaaa1348338452238fc3af6b8b22c87f88637ba5bab96f8fa2fccb`  
		Last Modified: Tue, 09 Sep 2025 01:25:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d6f03f4326881ba9bebf5f9d90320c5be6ba6943717918ed0e3742f19dbea55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e609b1f98cde36e36e07943b5efa22383057b5227da388c1469e5251bd7da1`

```dockerfile
```

-	Layers:
	-	`sha256:21564f8f9ad347b408bae62166baeaea02d513edb81b8fa68d02b285af03befe`  
		Last Modified: Tue, 09 Sep 2025 03:44:54 GMT  
		Size: 7.6 MB (7596183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d67e45a4a4d8fea620a6a4c269f1681d92b459b2860778f40307eac2717ace7`  
		Last Modified: Tue, 09 Sep 2025 03:44:55 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f479219dedba78976e69ae14b06ab2dfb06f93eb8353324a739fb31679c0f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196221670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7a1ad5821dc0bd6f307e4b4586503e6a260ed46b37fd22a3975513493e38fd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d54dd09e62bafd2c468d45ba15c0cc4fac551a0753fbcc6e5e0bb5cee582ac`  
		Last Modified: Tue, 09 Sep 2025 08:52:19 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8397a3e729905830bc0c43dc0837902d66ab0ffc11cbc4208a1bd8b831f7fc3`  
		Last Modified: Tue, 09 Sep 2025 09:00:07 GMT  
		Size: 91.0 MB (90951226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0584f5325b725db7a6cc468022c72c0d9a653df70cbd0babda0d6d603f19140`  
		Last Modified: Tue, 09 Sep 2025 08:59:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:37c79d54ba65f26ae316b94688f4f55d0981dd951f6751c42811a0479d12ec45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67d8b9c57d3c1af2672c920debc0e6a5d3faeee89b12c4edecc9d1d07dc6f58`

```dockerfile
```

-	Layers:
	-	`sha256:238b15702d3cd07513c5eaf5b513012ccbdd16c233a3f52a1e7e1624a5e43cd2`  
		Last Modified: Tue, 09 Sep 2025 09:38:12 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba9af6c2df41b9748eeda324327d21565a6e6f11fbb8cb58d9a60138e5aaa74`  
		Last Modified: Tue, 09 Sep 2025 09:38:13 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
