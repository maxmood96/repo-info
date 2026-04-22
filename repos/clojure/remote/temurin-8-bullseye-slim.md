## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:adf5587b74d4030c98978e1b6fe8f1a78fbe8d16edfecda70fb2917ab1995873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0055fe3bda39aef223ec88f4308417d10939e9b0c642dbc42611c49352db9d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144614871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f3ee1d50c1e8ebd30e6950c6a3a0e0ee577535e1942cbee5f574ac4832bd31`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:16:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:16:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:16:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:16:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:16:11 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:16:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:16:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:16:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff132b4e8b6933125067eb21586bf8129f9d157211d193ece2f4e5570492113`  
		Last Modified: Wed, 22 Apr 2026 02:16:40 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8141fe3de21fe79337016d55b90246c3fbedd4d57039f7eea5694b12174dc18`  
		Last Modified: Wed, 22 Apr 2026 02:16:45 GMT  
		Size: 59.2 MB (59186234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ad19be0888432d17c16e2c5ba53faf2422e81b2ccfd5b031c6e5a4f726c0e`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0953b27570f5df56f8ff705c245ec49e6b31716f95d7b434311730500907359f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321435bd524d95b050d63e66df7404b4bb1ccca611fde2ef3fe8d7329fe0c312`

```dockerfile
```

-	Layers:
	-	`sha256:d35930c053a66bc1a5c43d71cc7c854ca3b9f33782b64dddf3478e03fc6618c8`  
		Last Modified: Wed, 22 Apr 2026 02:16:38 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7bd995d314e10604c790a863016235aac94f00c53498b9941d57202ba5bb3d`  
		Last Modified: Wed, 22 Apr 2026 02:16:37 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75e4cc3423d07d1255da5bee2e9483958339d95fea30ee5ee50e67c33e02827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142325734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf9c70a8959d7374bc503b34ac901ff7fe1bd1281e7904b1fae6e2965a6e5c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e987a1751168f0d5cf46e7c6ee11ad761c27c87ec025093d6aa6de5b9a5c67`  
		Last Modified: Wed, 22 Apr 2026 02:19:32 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ab0f56a56ee199ff8b41df151b477cd3fe30626f8248d98bb40f062f68c35f`  
		Last Modified: Wed, 22 Apr 2026 02:20:07 GMT  
		Size: 59.3 MB (59330956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d8a34bcd7cefce7397ac50b5d8238b2c24152297a295648e30bb1220c620d2`  
		Last Modified: Wed, 22 Apr 2026 02:20:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1887fe07b20e1c3f9cce8c1b66635ceac49c01380172657e5e5735c97c976b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d99f2bc53664f4b45ba5973ebad98e529844ca39956daf7f0769b32499a9ee`

```dockerfile
```

-	Layers:
	-	`sha256:62a80bbfadc8fdd63157a11fb23d754cb115cad2dd95186001f3a98eaf15234f`  
		Last Modified: Wed, 22 Apr 2026 02:20:05 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f29d6642c198c0ca18aed1abb41dc3e764c51866f37251bf9ab9cfccbe7a589`  
		Last Modified: Wed, 22 Apr 2026 02:20:05 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
