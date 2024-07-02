## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:8d3c799dae27a32b1f39d92854b3ea6c3c6db246207ca128e6d5bea4667d1cab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:54933a65aa22607bb4f65553202d7542d661f9c7595b75d0272dd622710d7a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227703302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ca892d897df509244f7f17cad4fc0d6f811ceb180c5c2cc8e403212fffd01f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db31d7a23f6f12406fa8034f22acda65d8eaec15414656205b8b470b5f4bb1`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 103.6 MB (103600181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d95dce44fb966741bfdb79d0912a97a36089c804890ce41f73968205ef0e572`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 69.0 MB (69021116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fb61a845f3d7363c2f6a5a014ba8996774092e862b936ad9f3361d4b6fd534`  
		Last Modified: Tue, 02 Jul 2024 03:03:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fe8c45224aa19262b10725378f38899ecc02d67e9c195e0fcca0a239525eb730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa23ec3c25c750cc4ada25bc76257fd35e0c515dd3cffb6563081ff4728c4f6b`

```dockerfile
```

-	Layers:
	-	`sha256:e12d8262d0574a746cd4d969c734ea493ed629f0e24e59481c1a4d00409162ee`  
		Last Modified: Tue, 02 Jul 2024 03:03:01 GMT  
		Size: 7.0 MB (7022278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725794e3a11087359d25074a774b247d5ea680813ef289fdbd81edc4ead0afa3`  
		Last Modified: Tue, 02 Jul 2024 03:03:00 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfcfb23a8d728d89449201d5d9ce1a34e7e6b8261e94f9cb14955a93c7787335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225369819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea7a8f2e5bf04b38e9206733c6e6b216fea06db1dfb8025bb1f7dc75476e527`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa4caacc3a1e1326d77d86134d7ff7c6a2d2448547ed3ea79282943e9bf562`  
		Last Modified: Thu, 13 Jun 2024 11:22:13 GMT  
		Size: 102.7 MB (102700428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4eeb2b4efcec690c350c7e3bee6d51b3ace6fb6ac81b1a3de4be97994e738c`  
		Last Modified: Thu, 13 Jun 2024 11:26:40 GMT  
		Size: 68.9 MB (68929162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa32573f55e5178cfcd6f2c73ff2be5511a2413be9839f25f2f1056fd10737a0`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dad028556975055dd46cb41b1551937adbe71269717eb9a8af2d09fa4bce6785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8c201b335c88868996eb33189f778502c3f420a016f08c354b83290b22bad5`

```dockerfile
```

-	Layers:
	-	`sha256:6f6e0cde1525227b4bdf5c94a5fdeb9f79ad3914684ec33497ca5ed3e5ecb157`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 7.0 MB (7027961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d17b0fe84b37e49ea32b1156e0b5d6a3099223b2d18a4c08d4d1460d41ed3d2f`  
		Last Modified: Thu, 13 Jun 2024 11:26:38 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
