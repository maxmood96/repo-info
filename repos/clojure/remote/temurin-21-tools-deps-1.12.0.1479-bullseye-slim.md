## `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:913ac399c588e87b8868206f2b458a1548a8385ff8f1cade1a1a4cfb0146ee02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:33346deec2524d9ee749b32bdfcef59b206cf9c528cd6c53927b07ee1e390807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247761469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ad06a48342fc96a65a73d5484f47a6802d30a0c3274d842e55cef9b3e8044d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d456ecc711ecd6f4598460dd07513722ca01ae080103586d3f4b078e92a9ad64`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 157.6 MB (157568675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f81a846d5b1d30621b54eb44d1c47f8e5b0ff445553ec1db8a1535acb37fb74`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 58.7 MB (58740193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a6ffc82910cb35fba8710f30461e17ce8bcd397e209a578019a9719114c702`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e165dc61b3c3e1994ff49fa843d6aaa07596a9787762be829d96cea29075286b`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90a937be4f7a41bf42101b598ffbac88c133f00db3738594bbd7e9253690e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522dc257c68a5f8d7aaa763221d3b404c052329f1a6fe45ac66457cc319451b9`

```dockerfile
```

-	Layers:
	-	`sha256:2bb6a0dcd4752306d24b775cd65e887f8cea4854211c2293a54bef528ab5687b`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 5.1 MB (5129155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0d9cca206b9863529755a9f9b23e7bed49fe45b170e0d73c52506c4032fc0e`  
		Last Modified: Sat, 16 Nov 2024 03:51:44 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8e40e76107888f118ea46cf1e8f2f73850e20a3ca586e18447bdee846ca6080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244761234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9f619e1088f5668b4db3a47f8152192cf2081321e21d3be5f6c721cafba2d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65761880f0d53d3a20a6b437a7598675ca1a3cb59cca575f1ee410b546862a1a`  
		Last Modified: Sat, 16 Nov 2024 05:40:31 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8ad42f9046999e51a6eae35e00b5b57e0b0f83550db81023febb679d71c090`  
		Last Modified: Sat, 16 Nov 2024 05:44:42 GMT  
		Size: 58.9 MB (58875525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed941461d5f6fa9502e8ee73e3aec39da8f9d73d982a9d53d3726b5a629be4a`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75325a85f4f9268abb6b3b864ed4621d57651bc4d3ad856cc7cc05a3a29335f`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:96e589d77dda2905362ef89da35bc74942dbbf92473f43b43a237e1539f768a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baa7b75dc40c752a709016510797127e910c04735e673693283e5fe265c6481`

```dockerfile
```

-	Layers:
	-	`sha256:53c7d0b542a3e076a2e548454d8c3372e47d4c18c915dd1e46305c3d3687e15c`  
		Last Modified: Sat, 16 Nov 2024 05:44:41 GMT  
		Size: 5.1 MB (5134916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332d6ac67d77c49698bf1840cb6423cd6cd99225d22e74fa41e6176112c7cbe8`  
		Last Modified: Sat, 16 Nov 2024 05:44:40 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
