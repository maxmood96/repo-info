## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:37db29130a6aeae430c1f8826340552ce6f43094c3485907376d2f6f6b6b4f7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd29953172f66cedaf9752749f5af2976c99558134ebd3c8cf71fdc4d3e2f957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3996846881522e62a232cd0ad35ba8b067d8ca72c9b315fe98d4f80b49e234`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c5763245840f0fa70de5138ce64370da24f33f06343a0929c200a51bb122`  
		Last Modified: Tue, 02 Sep 2025 00:17:18 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c14d7f3e21e4dd79611f8de374ce4a77b5ad9a6db6733268845d09d4ee749c`  
		Last Modified: Tue, 02 Sep 2025 00:17:19 GMT  
		Size: 69.7 MB (69676379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d470a0c7346f0ec4f4726d56a49723285e6cbaa2253af4863d4fc55e2401b`  
		Last Modified: Tue, 02 Sep 2025 00:17:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1330dda5f3d5907473036667db176c2b68d0e498be02e5f0af14516f80a42f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f27be4ddef7669b8e20ec5acd7c5435cc0659192cb31f22927da476021ae8e9`

```dockerfile
```

-	Layers:
	-	`sha256:7ebdf1a59e4611f68257d9e10c4ef377c8908c3031d4d337b3cca8ddce52bb7a`  
		Last Modified: Tue, 02 Sep 2025 03:45:19 GMT  
		Size: 5.2 MB (5232883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf80911d4e43ebdeaa091233a54db56b93797ba91eae3044b829e57a4e8606e8`  
		Last Modified: Tue, 02 Sep 2025 03:45:20 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:937b126609dcccc73409d47e524d8dea4a09de6609ae0953d6eb96a4f872496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151467823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1744bddfd13708bac39c256f21c64851de9d04acb115c5f93fa367bb0564031`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3309a7dc8f110067aed1886965f5594bd9140ec2209f48b42b4293811b78484a`  
		Last Modified: Mon, 18 Aug 2025 16:53:43 GMT  
		Size: 53.8 MB (53835631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99da70b415c59a77e4a596d144175c168019d90ef1f88cca36c5278eb01dd0c`  
		Last Modified: Tue, 26 Aug 2025 17:28:55 GMT  
		Size: 69.5 MB (69549545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210dabf3b8da00024b21f85ce331338a607f40e42f00d8d38d18e985d9fc2fd8`  
		Last Modified: Tue, 26 Aug 2025 17:28:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7b1d349f54eb9ce7a1819a47d15a798ffbb1fac037380377f96b876b40cd863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b3386aba63649ba5fb093d39dadd913d243bf47ebeb74ab63da5b3de226052`

```dockerfile
```

-	Layers:
	-	`sha256:bce3d43fed3c054020c193e288d8ef6324331e023323e5b748e89cbebc99d09f`  
		Last Modified: Tue, 26 Aug 2025 18:44:45 GMT  
		Size: 5.2 MB (5239342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e0714e5246f08137929b3111812004b9d80ef999b9706b8d9cdbc2e5a54145`  
		Last Modified: Tue, 26 Aug 2025 18:44:46 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a1c958c3323a7be479da15add4c0423f5243fb61b7fab534d9c6eb96d32225cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159743614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b994583fa3c3d9f9adec35c878948ca4d4f638471d60e342774eacc3b20c1a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be65ab5f26e430ea2e40ede7e94ae14496ee1709a03bb8d4eabb0c050a62d0f`  
		Last Modified: Mon, 18 Aug 2025 16:59:44 GMT  
		Size: 52.2 MB (52165423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b8c9f6cd5c1d258c28fb4dbbc6996cec383bbf8ae2d80bdaf67819d1d17f98`  
		Last Modified: Tue, 26 Aug 2025 17:32:21 GMT  
		Size: 75.5 MB (75504125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5572a81047c3dc9c3665fadd713b2f5c94f1f1240a53bfbadacb63c485346b`  
		Last Modified: Tue, 26 Aug 2025 17:32:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5986d7bbf9bd93dd9b5e651d027f9fd7ff21dde32b670f733afa7db639226dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707892c70026172c5e46d30984cedad41c55b5696ea4cf3057ce1f709bde7085`

```dockerfile
```

-	Layers:
	-	`sha256:9a2fc11b97c496b8d4faeba79c63001b71dd9b7e257b270210eeeb174d20b39e`  
		Last Modified: Tue, 26 Aug 2025 18:44:53 GMT  
		Size: 5.2 MB (5238634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c87100406db0871c1fcac9542f7274614a0c0642538d25641afce9da481472e`  
		Last Modified: Tue, 26 Aug 2025 18:44:54 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
