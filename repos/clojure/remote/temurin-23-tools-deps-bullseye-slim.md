## `clojure:temurin-23-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b964e49e9b3aff75d03d5051a8d9e4f39d8dd6aca2adfd12a6b76ef889894c6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd9d9269cde0fb3ceebcd1f46ff79899652c656a9992d2446afd1608c6994ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254355524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5225df35bcac9937201a2b9d860a8a1997397cc3280e9fc83fa6596578622408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3b83f474071ca1cafcd7a66cc4b59d6e1a9cfe7f52abd1431a60a9dc9ef66`  
		Last Modified: Mon, 17 Mar 2025 23:22:09 GMT  
		Size: 165.3 MB (165316139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4b5d89a54d08e8faebe2f5aba12c218f28fc5bc333a1dc48460a9b70a7b73`  
		Last Modified: Mon, 17 Mar 2025 23:22:07 GMT  
		Size: 58.8 MB (58784509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51a33d4237da2c77222623ad18b113d4510d1a74a9c694099105f1141e7bdde`  
		Last Modified: Mon, 17 Mar 2025 23:22:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981f460ecfb5ddf698aa86996dcc202dc16227fa8d8aea0a1b73df0e7223ca23`  
		Last Modified: Mon, 17 Mar 2025 23:22:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:993c707b446b6acea2309423ac26528b72c4cc8999aaaed46e5d34c2ef87e7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fa5388b4f50a44b669d478dbe04e36763ccd7a41a48b383d46cc2a2a2d8e1e`

```dockerfile
```

-	Layers:
	-	`sha256:ddacd8ed8b3540193b59b07beded4307ef101a53c9e74de3b5ed5228da6b7f5b`  
		Last Modified: Mon, 17 Mar 2025 23:22:07 GMT  
		Size: 5.1 MB (5122072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b6bc2c7025b62e2076226c97ce3edcda56db19a77e0b5c14ab7f2cdaf10980`  
		Last Modified: Mon, 17 Mar 2025 23:22:06 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebbc7c1a6253c1d97af1ac6d57424c2ac789da558ec38fa5e4a6dee0f211a1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250996879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db792f3b6dad59964b10ee0605750eebe00853f0ffe832db1f7bd363550598e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de4e1b652972a2ccd884dad7e9173cbd706aa25eb867acb8ae875d71e4d525d`  
		Last Modified: Mon, 17 Mar 2025 23:57:21 GMT  
		Size: 163.3 MB (163341467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7787d50044cb52e928dc0292d4b1448ea0c7de822d4d0e86b05b5d7cb6ee331`  
		Last Modified: Mon, 17 Mar 2025 23:57:18 GMT  
		Size: 58.9 MB (58908449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e89e49635750634f54f95a986ae2c57f0a614290eae33e48a77529d1008d748`  
		Last Modified: Mon, 17 Mar 2025 23:57:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1810ea50f5eef5f0b92b3f65c2e7cdbd914c03fddd0cbd3f3d766c0c7b3048e`  
		Last Modified: Mon, 17 Mar 2025 23:57:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0f0aefd1a02b7e81165a79d87fbe57fab8b95dfb288aadb795c19dc6b8ba386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0827220f13adb02ec22a356b610dd0e082f2222013fbb596ea6be83340dd619`

```dockerfile
```

-	Layers:
	-	`sha256:d6f35400c9c9ff87176ce6b64064d1f9e6c8f4f9b5eac769d992e7ed6eb6d651`  
		Last Modified: Mon, 17 Mar 2025 23:57:17 GMT  
		Size: 5.1 MB (5127183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90b1bbc3e3a029a90c966134730714fcef9fa127cf23c98c084ac89c43d1162`  
		Last Modified: Mon, 17 Mar 2025 23:57:16 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
