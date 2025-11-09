## `clojure:tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:ef62b455a04a7d8c7ce22f66e77f7aad01be97c8489639aca2954e5f7527c1b7
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

### `clojure:tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:c42e3728b2415e50bf9b46a4766d5075415330b4e88768c23b4cc2fc8ebee083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221673861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc26e2f9289a99a8b9d0101f3224d1aef59e84d42b347c0e66ff23746ba19b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b674e491f57ee535dc9120be069d629dcae5441e94fe0d341f026b220b941502`  
		Last Modified: Sat, 08 Nov 2025 18:47:08 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139f0d48a590359c2d3cccae19c172aefc312948de502ee1b3ac20e316fc0b10`  
		Last Modified: Sat, 08 Nov 2025 18:46:56 GMT  
		Size: 81.1 MB (81146460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5698c579b16f015815c41723cfc428f4d5e4e0a42b1aa1f2f3d65f3d22f45`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b9f4d675981411f99aa73d2506450c695237d7e245e93e6ae9df7986050c27`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:e4ade39af07bcfe9c1b15e8cb70397dc8f7f746c9e5536065b94c695c6608787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c92242fcefbf6644ac3d690bca83eb2d3e89aebef765bab2a24c121a581367`

```dockerfile
```

-	Layers:
	-	`sha256:294bd1b9633d832c8e4b4f24eff38fbcd8e8d8ec2c3527b5c4b4633f3548de2f`  
		Last Modified: Sat, 08 Nov 2025 22:50:57 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c21a6cb33cf6bb3b253d08f9d23fea7181d7517a2465048477a522ba7cf1766`  
		Last Modified: Sat, 08 Nov 2025 22:50:58 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:530081f2c4c5c130af38dd69ce5334712f2d10e3ff9a88a4cbe2956b4947cbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220443910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7424ae60f9fbc7546208217c0c47e9cc8d1dd4878599975027c1adc3d41bfe9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:41 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:56 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75f74857479ee193d23548457f622f80c59a23c8c0f7933d8756a5170911b13`  
		Last Modified: Sat, 08 Nov 2025 18:46:21 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0349d743861c0eb912e2c43d8fd87f5c6570017b2deaf79b94ac071e802389d0`  
		Last Modified: Sat, 08 Nov 2025 18:46:44 GMT  
		Size: 81.0 MB (81030886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39577c3b42fcbb9f659141fdf9691d4a04439f468a62da81fe805ef86a5eab9`  
		Last Modified: Sat, 08 Nov 2025 18:46:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ae6c71eb8bd58d563262d228ec84a9c634e37984d38a116b852e96d9fc7df3`  
		Last Modified: Sat, 08 Nov 2025 18:46:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:0190d60f40a61c9d1fd2586b4ce4f5ec8331ad1ac1844e1a65759bfc1bdb20e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a935b80a19b66b2d08620a4ffc891b1011ad09729d3b8134588b4bc85b49fbbb`

```dockerfile
```

-	Layers:
	-	`sha256:450617982f07b9346586faad52a91486f9efe92738dd45d843a12bac9086ea60`  
		Last Modified: Sat, 08 Nov 2025 22:51:03 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d44c6799b6dd3ea76b1c66c734ad917b825ab67c8dbb30e8c51407317f9e285`  
		Last Modified: Sat, 08 Nov 2025 22:51:04 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:665cfed5777ea8f1e91f560841ce68e07a5b9ac4a955bef0ca27dbf11efb0d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230925315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ee91bc582a53f67720437e41163990e18e780b2bfe83688733fecd03f2cba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:11:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:11:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:11:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:11:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:11:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:52:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:52:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b1be4bd5c392224945402db7277dc7a8f213a2d808e9ddd6b01efa46c2c1a`  
		Last Modified: Sat, 08 Nov 2025 21:13:29 GMT  
		Size: 91.6 MB (91610767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b53a303bb7098911cb11710ff348d8d274a962cccd6b3924c7106620c26d78`  
		Last Modified: Sat, 08 Nov 2025 21:53:49 GMT  
		Size: 87.0 MB (86986225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d49d985ca40af348c438f4bd81b4c22546685334744930197628fdb7b9ec6b`  
		Last Modified: Sat, 08 Nov 2025 21:53:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751be8eebbe96676ff64d7822036001f885c481f44b2d45f102d91f7175a05b`  
		Last Modified: Sat, 08 Nov 2025 21:53:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:b5a80d6808808b59a8d155e08a340be7744655896f3828c9d21f40df90aaa0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0fb4fe3de00dca15a0668c33f280552fbbbda01e39dfc6971a0be39231ddbd`

```dockerfile
```

-	Layers:
	-	`sha256:0c6f481b7a155679f7789f7a5bbd4548e415b0331ead8376eb39a4e890f9925a`  
		Last Modified: Sat, 08 Nov 2025 22:51:10 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1e65f223090b13103401c4c239a270b6c77dbbdcb33137d5e74570eb63e1e2`  
		Last Modified: Sat, 08 Nov 2025 22:51:11 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:c5e1aec60e538440f9afff013e625402a8f22a9439a30b598698f5446b16c5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215306437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76881d90a05894caf8e2a95bb02209eabb96e67fe37be98174adbe925c9afeb5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:26:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:26:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:26:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:26:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:26:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:41:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:41:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:41:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:41:45 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:41:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae75030561f486cc06d185594ec7a542d92180c2f5992e92b8dd3ccfe9149e`  
		Last Modified: Sat, 08 Nov 2025 20:27:32 GMT  
		Size: 88.2 MB (88210702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bac989aaff73d901dd3fa9777712971238b347950b759dfa96ef0078f3cfc30`  
		Last Modified: Sat, 08 Nov 2025 20:42:33 GMT  
		Size: 80.0 MB (79956600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb27c8d34c6efb8fc7cce368cd127607616cd04888adede96cba5f6a835527bb`  
		Last Modified: Sat, 08 Nov 2025 20:42:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5deaca194dcc04fa7fd0ea7aabce83a3a77cb085516ae564812d58977f6b14`  
		Last Modified: Sat, 08 Nov 2025 20:42:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:257d6b6700e7d756f88559a655afd1a82e0ed3505cc39e1bdb2e0462b28366ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea24c4b1ccf1c462aa28ea71564ad6eec439729917c329789708e5772eb246e`

```dockerfile
```

-	Layers:
	-	`sha256:645380b791340203be691dea704557cf8fad5e6c50757747f1fcd8de1aca9967`  
		Last Modified: Sat, 08 Nov 2025 22:51:16 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc64456659a49e9d2a564c89b5cd0ca6fc3a58ff74f7ceb242dcf4f401c9c869`  
		Last Modified: Sat, 08 Nov 2025 22:51:17 GMT  
		Size: 17.8 KB (17770 bytes)  
		MIME: application/vnd.in-toto+json
