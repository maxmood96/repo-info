## `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:b2dbcf0a39dedf88e09f191028a3672381e78f40913dc03b18dfb6b3b75a0871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4365f564e4fc060aee6b479160ff9012f4398464bd42bd0250558e4dd7c7f2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287438449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4485a1af5dc021a0d49d9130dcaf98fe92f40154e260caef5ec35978985e54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c58c61a8aec0f2102b965a60dc5c5e71f5a36578a7d250b307bebf6b009ca00`  
		Last Modified: Tue, 26 Aug 2025 18:47:11 GMT  
		Size: 157.8 MB (157804772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755672a72ac69b10944d42a899ffb034379f7b89bb6a2901c84d3a91d51ec40f`  
		Last Modified: Tue, 26 Aug 2025 18:47:03 GMT  
		Size: 81.1 MB (81138121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097966e584e176dc040439b8e178f09d2a462a2aa33e98cca02252afd9760f74`  
		Last Modified: Tue, 26 Aug 2025 17:32:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750578e030b19757843569de9fa0c2a8cf9eeb2bf809f7fa97ca7d31757ba8b5`  
		Last Modified: Tue, 26 Aug 2025 17:32:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:de9b4e23e1523969c41290fb8ff2ff3ec71c5ec7d72afe5412d42d384067bfa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd27127d57afe3586cd3a0c2988c13921a01f180b3c1b64a781e1005515685b`

```dockerfile
```

-	Layers:
	-	`sha256:c70d51ead3204cd96bbcd68165de0181957fd9dbe49698827532772860b18c3b`  
		Last Modified: Tue, 26 Aug 2025 18:39:36 GMT  
		Size: 7.4 MB (7373399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc682618a6ba06cfbd91eb76600c993f1bbc31193dad8bff86747891d15018c5`  
		Last Modified: Tue, 26 Aug 2025 18:39:37 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f9514dad288137717e77853b1dfeddc786056526f116b5d3d7d864e64ad88f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285434058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7923e0186787c650956d9b69d8a49494b12e55899378587e8dab01264ae30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f78888ab9c57e95226c3244d90e801f0c238e605329f20de72d1f2676edd7`  
		Last Modified: Mon, 18 Aug 2025 19:02:08 GMT  
		Size: 156.1 MB (156081244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205c07254b8c53a7d97a9035f701a958d2dab1d4e867144cd9fd36532550dec0`  
		Last Modified: Tue, 26 Aug 2025 17:48:07 GMT  
		Size: 81.0 MB (81009318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f6665b407306a983bc0579a04e40924af81610feebe03b253643ca343283c`  
		Last Modified: Tue, 26 Aug 2025 17:47:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96419ea193fc8fd244e5b78cf2b6b0343e22fa8611e9c906871b6bb68fda0548`  
		Last Modified: Tue, 26 Aug 2025 17:48:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d63310d67a17e28556844dbba30471f132c9d71c2d639bed66021124ff90123a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a85c6e01f1e251f28ee6986ca7f8087ff54fd3e844fdc385cf70d1c47d469c`

```dockerfile
```

-	Layers:
	-	`sha256:6e85cf7bc8e6d5993c7dd90db5f708c60bfdf883ec2be232875032bb44e6f245`  
		Last Modified: Tue, 26 Aug 2025 18:39:45 GMT  
		Size: 7.4 MB (7379234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7d59ab69afffab718aac9f220bbec50f27ca534016126f80b7cf11a1d0055e`  
		Last Modified: Tue, 26 Aug 2025 18:39:46 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:264204194fe7ccb9691d7c4206a7557e3ef2463b5601c9606b9fdf32172cae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297275390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232de03eb48ef196277cc6d36e5eefd1685873b0b6760b6390cf79a84ec5ed33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e33b25faeddaedd56d237955b1d8704c3e5726b3d03e54c231305f0da8d7f`  
		Last Modified: Tue, 26 Aug 2025 18:05:10 GMT  
		Size: 87.0 MB (86972794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8451491ebeef5544187d4211fbbdad7deb87708f14b9678be35d49a988fa096`  
		Last Modified: Tue, 26 Aug 2025 18:04:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ac2e5e17ebfb129301aa3d86f2586065f4a3c6e4a3dbafcd8addcf3c5293b`  
		Last Modified: Tue, 26 Aug 2025 18:04:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:35deb2f4e84695c0553518ffec8fb46c0da62358947d2ff36c4950764a20b1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eddddb932d77948adb6fb753ff30925ae4f11d28d8ac24192fa07b5d0bec13`

```dockerfile
```

-	Layers:
	-	`sha256:259488a0908079e202da03f96cadeed7b7ff7989b96f593707a39c6aa0fcb3eb`  
		Last Modified: Tue, 26 Aug 2025 18:39:59 GMT  
		Size: 7.4 MB (7378639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09e91f345d2ebbc1924f7d901743e74bb1dae82dca836e8513d40b10b1fe2fd`  
		Last Modified: Tue, 26 Aug 2025 18:40:00 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json
