## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:109e23b301ddb82a8397aabc836b88dd74b1e5ab9aaee4638682308a3541f7b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:849ab1cb666ff2dc22215b13b173c69ee6ea41e8df92c2d55e4d98dfa3c0076f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152638698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4664c5f6ce5ef2ed40bcb53c8c2977bde3c9929c5db1d3cd46f9df5b60357e16`
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
	-	`sha256:8fcf18bf001a31a19aa45df6ef3a29b6ebc929b0332a0c361d9f56c51bd6fa4c`  
		Last Modified: Tue, 26 Aug 2025 17:27:10 GMT  
		Size: 54.7 MB (54731349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e526e701fffd2d710046b9f119a6fcb49da265f35338104fdeba122629943b40`  
		Last Modified: Tue, 26 Aug 2025 17:27:10 GMT  
		Size: 69.7 MB (69676450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca194d06fc9d9b0d396896201f8ca966976c6c2fa5a90c4f7bf972f2f455337`  
		Last Modified: Tue, 26 Aug 2025 17:27:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4e71f71cf43de3a57222ba99ca7941c4359bc8a9b092c12200f0840357bca61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777d55fa883407cb1f6276979887f15865764171b560dd5954e713dd4caaa48a`

```dockerfile
```

-	Layers:
	-	`sha256:fdffdbaef46816085858976ed9576a4f4931b83f1125afb83d240414c3b938ec`  
		Last Modified: Tue, 26 Aug 2025 18:44:39 GMT  
		Size: 5.2 MB (5232883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6f819f89e4b4500f99703fb0a8ca12a0848c929fc2ad0e575f5e878238a0a4`  
		Last Modified: Tue, 26 Aug 2025 18:44:40 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

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
