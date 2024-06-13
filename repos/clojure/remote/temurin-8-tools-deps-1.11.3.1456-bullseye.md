## `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:82fe975889d8d5db631b45a8d4facfe3fa8f19a74a77007117d665a6460c80e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:44d27d3c54eb3ef23dd3d00b79e0afd53baa1c9698f03e0a24213c1a48ad6bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227516493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e773546dc377e30f048be406e3e8a3dc01b422a322b6439e071d12f3a7f5dd6a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083badfe8eb49c2c8112efbefc1be8401b4df21877ab2d9f79b1815311e1622b`  
		Last Modified: Thu, 13 Jun 2024 18:13:56 GMT  
		Size: 103.6 MB (103600203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd46487f09c81ddc966399d4ca845b913abeffafdd5ed0cc2a6772d0445ee34`  
		Last Modified: Thu, 13 Jun 2024 18:13:56 GMT  
		Size: 68.8 MB (68816452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ea65ecf93a172a6dbd8ff8f2d74bcdef204662b0f4853f7343a1f854437465`  
		Last Modified: Thu, 13 Jun 2024 18:13:55 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2b05a78345e24f3aef4ac66b76d48c78de514d88a03f32356b44347114e51deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7036090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8569d57398a0878208da92bf53fcc3d0bd525ce90c627d381bfcc48d9c508f`

```dockerfile
```

-	Layers:
	-	`sha256:3b5efc6eee3516d74c42179ce6f642be341ff8eff407465fdd552f1ab70e547c`  
		Last Modified: Thu, 13 Jun 2024 18:13:55 GMT  
		Size: 7.0 MB (7022239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7666936b1d10774f676ae19a821d70c3036952c055294c0d73e7d48eb71d9f`  
		Last Modified: Thu, 13 Jun 2024 18:13:55 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

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
