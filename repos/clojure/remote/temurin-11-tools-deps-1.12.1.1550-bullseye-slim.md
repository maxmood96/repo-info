## `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:8519919c1e1cea3e0be9c58dd18fe7611f9504d3eea6af5574414f6ec0d422ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:55b12882cf22230af44d0ab5152b1f206049e9e4bfbcf1eb44eb16b320380bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234898019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648d76a1e319e82d0a035cfee5352d4db12335c31e8eaf5a316d56fb09a66903`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c7774a1a4913611c3dd2e2b240745154faaae8d7908678a48c7d936a724d96`  
		Last Modified: Mon, 09 Jun 2025 19:54:32 GMT  
		Size: 145.6 MB (145635675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41672834ce341d7309f3c3145fab64b9896858aa1f3888c7470a83e725070d52`  
		Last Modified: Mon, 09 Jun 2025 19:54:22 GMT  
		Size: 59.0 MB (59005759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f91ec94241766cef050eefb6d6068a21f65bb59ab3b649ecace1d2b9b33b190`  
		Last Modified: Mon, 09 Jun 2025 19:54:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cac34f25b8c1ca530ac695abb886caab8769a25518ac718f3de86b679b8a3b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8c711a5927702d7f49ce007e482e861b12e1c8e2844f1e784720b6babed33f`

```dockerfile
```

-	Layers:
	-	`sha256:bf70974cdf3bc38473d791d487c7deeda7e146c08849cbad5d5a1846ac9730c8`  
		Last Modified: Mon, 09 Jun 2025 18:35:14 GMT  
		Size: 5.3 MB (5329803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6ba01a5047ef8edb7744f1084e0fa245d4181189dcb0e2e3730836691da9f4`  
		Last Modified: Mon, 09 Jun 2025 18:35:15 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7fb3de216d9e0d695d0801af71adc1e58ea94ab3bb4ffb2926da7a41b0d4113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230305113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad8b87ad14a735dbe1f0af14cb54381726962d911dafe28bbbcc82046eb55b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c7e75dcf364b2ceee07e82338697627a9716867e83933b2f790e9d0962da2`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03568ce2f109909a948acb2f0c66270b88e149bfeb70e4d4399af6d4c2226352`  
		Last Modified: Mon, 09 Jun 2025 19:55:01 GMT  
		Size: 59.1 MB (59137546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71fc32bfd29bc6be295994a0d8786b36f93ad0a31b943f9c68f4cc5fde8d49`  
		Last Modified: Mon, 09 Jun 2025 17:49:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb241784e13f9fa854afa97f396489ffabd7e8aeac0e6fa62a521f7cb6c37395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4845e6bda11816fa44ebd48900667867e72817a968a9f5f394bf53ee8bd23`

```dockerfile
```

-	Layers:
	-	`sha256:ca8f2cf408568bbee1e34f7d3cea93b17c1a746a0b5e00ec193bd7c5c3b2cc57`  
		Last Modified: Mon, 09 Jun 2025 18:35:22 GMT  
		Size: 5.3 MB (5336153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedf5281fb2191a2ec3d1d391d444d368a0f4ff38bf52ef46e95effb9fef3799`  
		Last Modified: Mon, 09 Jun 2025 18:35:23 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
