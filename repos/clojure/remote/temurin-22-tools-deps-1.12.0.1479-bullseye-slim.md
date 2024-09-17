## `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:bbe6973e403bad18a88e032f5e687a8bef24e14497fc14058d056ba16dfa8a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d7d4bfb4f8e14bc09d643c625ef030d3f201ff050eacc6c205fdeb0605a9fa13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246852124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0738b2a9f0b3ca6f6295da25935f3d47d7af56917bf263dc7d83c596b0b0aa67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ac4883076250d708f24bebf5bc8ad05092e801bbec2546571e2b43e729304`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 156.5 MB (156481644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce09c70c0a8818d92a18eb6c35b2e62284bbb6b5c82a9b01da9025de95263b8`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 58.9 MB (58940757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b1a00c1b97184b036eea5bd633f39a881aab6a0a7b124f6459a173b9b7d95e`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40f81120dc75ccc22eb0a5a8096d0a6902755247b6cca25b7ec39404aa322e5`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7e186813e0d629a989233d42353d226bb7db201e534b58b23c9dbf42d7ff9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859f3748fd4376e96ceb40194304ac2ec21babb27f2149fa1fdb2ffc93e093d6`

```dockerfile
```

-	Layers:
	-	`sha256:cffc1164536f9ddd9edbc62bf657dc681e9734db8dfec398354f82e00aae58e2`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19c7e75f8d1236178e04c36ee4f53a93b57107bea7ea8d00f5f06812e62a288a`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7107a103a45c4825afbd45418ed01dc5ee2762b1922f7cc05e2cb8844722483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243650705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d830fcbd7d375a81075b0aaf44485ec7f3fb82a94709d8ba6dbe4e20f285d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50350f2974c0417f312abfa4209238a88e094d8f3d7ce45496c26f6a51b902d2`  
		Last Modified: Tue, 17 Sep 2024 04:54:51 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046c278c6af29b50470f4f0fd30fa4c61341d1fea06c228fd3d256023753faa`  
		Last Modified: Tue, 17 Sep 2024 05:00:00 GMT  
		Size: 59.1 MB (59071538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23693893a4f5f34d714886d31c9d32eebbe9e86d45fc1085b45c1d2f7ff5add4`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f5fa3d745ac9a8d1e3dfe4f65a47abf87f6299eb1befe8df5279a9ac1f2d85`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f401b603b7d99c96b566d3c384ed0b0b4d9b2e2b8e9882f74f3713db6541b138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd5e7cd084cb1740f35d096916af691773d776b566ddebbb7037f27345585eb`

```dockerfile
```

-	Layers:
	-	`sha256:288c8849c625464960c75db80a80c309f1c23a92481505ddd0875478d7ce0470`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a3dc2b581b090675d6d38c04a8c5a45f55c9649cbd424920dbac7ff1c05cb3`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
