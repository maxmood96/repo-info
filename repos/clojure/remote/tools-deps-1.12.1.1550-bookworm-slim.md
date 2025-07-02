## `clojure:tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:3286fa82747b259a3b5122001819488565f9feabacc7a77ce107801d2a75d3ee
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

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7f08591c2f94aab1ba821fa23f1ff608931215e15c3a3e4a44de1c02d8455d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255399000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e18faea2167e3f1dfae30e41469075df8eb41add4a96af9aa78bc2cd2e0eac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8620846a0622ca2e69fb27c9f932acf94b387307a9129dd630a0db956227d0`  
		Last Modified: Wed, 02 Jul 2025 06:44:38 GMT  
		Size: 157.6 MB (157634442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bb917f7f33c93d254b54fc8481122459b3e4778e07a732719522a79b639fe`  
		Last Modified: Wed, 02 Jul 2025 04:17:17 GMT  
		Size: 69.5 MB (69533378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b69e61d07f0d80c49f3c70e36738d597af17ea933c8d8a04025f601bcdfc652`  
		Last Modified: Wed, 02 Jul 2025 04:17:05 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa0075be15059d5ebfea3302231c9c4125aa23dd733175f464e036fded302`  
		Last Modified: Wed, 02 Jul 2025 04:17:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e7b7a4fd390d0737201278bd4de47109b63c6d103fa00d8ca14bbe6d834dab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35287ae6e2c13ff3e5d8c5ce2c35391abb57ba64d93e1cb4fc9c7edbd41689c6`

```dockerfile
```

-	Layers:
	-	`sha256:5a835f2771e5b16d1d49189804d7137156364a350cea13cc30c02480de08ee27`  
		Last Modified: Wed, 02 Jul 2025 06:39:15 GMT  
		Size: 5.1 MB (5115042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9145c0505e2f6fa251b16edfffa107475c8374699017900c946d013f76e6eed7`  
		Last Modified: Wed, 02 Jul 2025 06:39:16 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5820b8ad5706c97f3ed5cea816705668d72bddad0c0ef1c6290eb2ed56df83d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253396447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ddabdb11d6aa25a1289dbbb03d30e16b6e91a800280138157140cb99f9112e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8daedabca9e0ec0569eed016beec20c98e8bdf92ec62e903cbb8b335f9a4c66`  
		Last Modified: Wed, 02 Jul 2025 15:57:35 GMT  
		Size: 155.9 MB (155928782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99821d0d9ec46f05a88e2d56dad2c90516a9e363287967658ffa74ccb516debc`  
		Last Modified: Wed, 02 Jul 2025 15:57:29 GMT  
		Size: 69.4 MB (69388946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06f0aee0107be23600741e63a6c8c4306d3c630363892c6cb08dc59a563a68`  
		Last Modified: Wed, 02 Jul 2025 12:50:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f654df14ad44e3818b88b9222f2e7954541867ecde6bc8253d88578538ee05b`  
		Last Modified: Wed, 02 Jul 2025 12:50:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:080684b3af050c79b51f8a26f35b9458359b106e6f58fc57bd7fbb77f751c110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d25f023f3e322e54d34c276a0915f659325503238926fd9d80772942d12d1ee`

```dockerfile
```

-	Layers:
	-	`sha256:ab23697e092a87942db80f4fd1f53684ad8af8a65ca226fc5ea9a48d949cd51b`  
		Last Modified: Wed, 02 Jul 2025 15:39:39 GMT  
		Size: 5.1 MB (5120827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c3c936d4c2a7ce0a8fe23b1674902f874acd6dc7977df0985be9ed693ae45a`  
		Last Modified: Wed, 02 Jul 2025 15:39:39 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:18723b02b7bcab7d0ef02da79edcf625954e1b6389fd7ea7e6e8dc7e162b19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265237000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508e3c051e98e8b3ae8838212cc9d70474bcff3655e19832ba74f3a4cfaaa0cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c624215c6956ee0071fac4e87b88decf6beb3fe0a83292aa42c1ce7d6b073d`  
		Last Modified: Wed, 02 Jul 2025 10:45:09 GMT  
		Size: 157.8 MB (157804888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be45c18be79a9ab0cbecb856cf85084ec29dddbe21469796efe3cc89ba12ffd1`  
		Last Modified: Wed, 02 Jul 2025 13:53:26 GMT  
		Size: 75.4 MB (75358249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869ae072ee68ad53b35567d5c305dd842fd0d992bab08c9312bb8f376d558d3`  
		Last Modified: Wed, 02 Jul 2025 13:53:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084b578ca7ec067e8d6bf1613248f4a1da24bd5a38eca62b4e37778c37f5cab2`  
		Last Modified: Wed, 02 Jul 2025 13:53:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d0d7583e3e42c31cc7048cc360b48b060b31fcf57fbd2389b4cadbb9e53ced2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7507810b83df0ffb713e554d41e212e7daed6f5602ece2a2116712cf29676c9`

```dockerfile
```

-	Layers:
	-	`sha256:4a9c55e19698d0773fdd1e893daf3274b25638b73d87fd5fb4a730b57db8ddbf`  
		Last Modified: Wed, 02 Jul 2025 15:39:44 GMT  
		Size: 5.1 MB (5120212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f40a5625341160c557e987bd1b3c328df8dcbd7b4ed105f3b6752784c1f5c9`  
		Last Modified: Wed, 02 Jul 2025 15:39:45 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7120ecf6f988de2f024c33cf27405d23dca0f9a78b83ce4b2a550cbbac1ac5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242138735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ba970c185aeeb64c11cb8e55fc1882a03f4d3c27579d28ddc3d5a08e3ed21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8573fa47c2bc5409f11e03c513f5b48e958af3b508908c4d9437b6726eb8b`  
		Last Modified: Wed, 02 Jul 2025 06:45:33 GMT  
		Size: 146.9 MB (146910935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b04eb3acbff8fdb293c2623ddaa80d1a747983e79c8c5d8677c4e95feb949e`  
		Last Modified: Wed, 02 Jul 2025 06:51:22 GMT  
		Size: 68.3 MB (68338948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53525d4a166c4345aa43b64336710f53ab536e49c0f42ad42b922cee2f844d5a`  
		Last Modified: Wed, 02 Jul 2025 06:51:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089fabfd3b631238af3300a5f3753bc4c39eee13b9b3fc522de5b25b83b6498d`  
		Last Modified: Wed, 02 Jul 2025 06:51:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:295345c371feef83fb0eacb490634e620d9455bb52711b32499446915aeb59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdea127db53c84be5ca017cce2e3bf4b9a2e9c451bbe1d667a8154145f918d9`

```dockerfile
```

-	Layers:
	-	`sha256:450ac29819b6736d32c122d8ce7aa16970652c249e958804f101006c890a9f8f`  
		Last Modified: Wed, 02 Jul 2025 09:38:57 GMT  
		Size: 5.1 MB (5106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4a66d245dd9bb9fe2df76dc108f90ffecb8581dddc131853e42f29d6aaa439`  
		Last Modified: Wed, 02 Jul 2025 09:38:58 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
