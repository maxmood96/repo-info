## `clojure:temurin-25-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:a50aad3adda4ae36f78b0a542cf6e9ff8c581a1de689a5865578f491468695b2
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e4df8660ac12ca8b0542cae8b0889f4e5f14c72a09746f4bfd0788667c0a928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226862845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e39501e3f08a1318dda71f0d826b4b89832ecd54ef545111c4fcb6d8074ee3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:31:40 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:31:40 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec5297ae368391213c8102a6643375ba96acd3ed2886daa49690b6df1a7e40`  
		Last Modified: Tue, 04 Nov 2025 04:32:35 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559ebe50f4204720fd9fd0a56b89f15046209d86f6767a68b5e6a049206f44d4`  
		Last Modified: Tue, 04 Nov 2025 04:32:34 GMT  
		Size: 85.5 MB (85540141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f440c5a00ecae291c8c83215fb64c9b3810104ecfeb13ebaf6bccedf0cb388ab`  
		Last Modified: Tue, 04 Nov 2025 04:32:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043413be531af7b85c9fd74ef0dbef246af7502c1879fefa7d90949430f81fcd`  
		Last Modified: Tue, 04 Nov 2025 04:32:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3412ccb2667ebb85133b4dc7154f8e3e0026ad76d02a38bb88096b9608091150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcdf937338229d5026072c95c64cfb938f67222779ecbbccd5ffc619012d027`

```dockerfile
```

-	Layers:
	-	`sha256:148c1a157c37c2c24917c6a4751da18f30a902570f174e547ab55fbb6095c055`  
		Last Modified: Tue, 04 Nov 2025 10:46:52 GMT  
		Size: 7.4 MB (7418217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac5b0f83dd69422d954dbe9b8fcedf3b5d03ab5bd5d6bf3b2087e96427d80004`  
		Last Modified: Tue, 04 Nov 2025 10:46:53 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7cf90f36f4f55905dcf642f25e4ef3d0a7acf86d4741be23ea740f8ceb65642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226059972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe6577def9dc2f26c4c46335d30a699dfa3450cddc09720d4ef34d065e9e02d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:45:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:45:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:45:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:45:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:45:57 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:46:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:46:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:46:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:46:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:46:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8515a948d397f2210db9420a6543e0acd44245e4cf843582bf56e912c3f5a8df`  
		Last Modified: Tue, 04 Nov 2025 01:46:53 GMT  
		Size: 91.0 MB (91045238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e155a149f85e1c81c22853d449743cfaad746e618e46a8bbb159a26296c42d8`  
		Last Modified: Tue, 04 Nov 2025 01:46:53 GMT  
		Size: 85.4 MB (85363269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b403e506dc5d47d1a2e5fece1ae2055127ec6e64c7892f8f86e72f67502ea`  
		Last Modified: Tue, 04 Nov 2025 01:46:42 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c095d6e53693cfab301f6acd0c10ca8aa6b6752c7a166d7479f5fc82a0759`  
		Last Modified: Tue, 04 Nov 2025 01:46:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62e5e273cb0e3078bd2e1708cd47870d584b6e09ae57c75010e31c229cdbf365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb8657d807802b0aea3c8f531501f86ae21aa875a8885d896a5767744c377`

```dockerfile
```

-	Layers:
	-	`sha256:4512477e73fc489523671b81e7cbbe36094fb85136c15325272b2031135157f9`  
		Last Modified: Tue, 04 Nov 2025 10:47:00 GMT  
		Size: 7.4 MB (7425268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4113a775ad5b4138066575ad4c2e3081476b28d732c84a7866e2dd93e56456`  
		Last Modified: Tue, 04 Nov 2025 10:47:00 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:cea9ed1d0ac8ab6a6372fe72d25ed704f229d411f15ff7fb085413ec7f5ce432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222950335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791342c155b1c6d88d1e1693f6b269e83f9fe2dfcb3ade0cd1362da26c4e7c5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
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
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085fcc1e1caf4b241284491b200911f500e9abc4b0a5e86b6bcb6d0860ff050`  
		Last Modified: Fri, 24 Oct 2025 03:48:43 GMT  
		Size: 90.8 MB (90752375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801e350f852cf817f4be953d2204699526eaee49499caba6c8d7209d4aa72888`  
		Last Modified: Fri, 24 Oct 2025 04:29:36 GMT  
		Size: 84.4 MB (84426611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293830657f7835bd14817c24a4ea5e9702e9df0f5577bdb0e70a67a3f6dc32c`  
		Last Modified: Fri, 24 Oct 2025 04:29:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cb029713b9c82d1e9da3acd4c34cda42dfaf1a5e72681d4137fb39c6faec78`  
		Last Modified: Fri, 24 Oct 2025 04:29:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6efac43a02044e63df81612ba21e03b97b27a8db4ff2fe2699ceadf8367c52af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db31d94a72bde0a95ac5e073dc55309e3f4067116bb0f765f70054c6777682b`

```dockerfile
```

-	Layers:
	-	`sha256:7c9eb8fc3a9cd9f7008284510d9d3b3114604a76d3dfac0d8288f160304c20c1`  
		Last Modified: Fri, 24 Oct 2025 06:37:38 GMT  
		Size: 7.4 MB (7406139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a07a145f70704aff899f2deda8900f65e45517f2cb95db07e2e3dae74793cea`  
		Last Modified: Fri, 24 Oct 2025 06:37:39 GMT  
		Size: 16.5 KB (16516 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

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
