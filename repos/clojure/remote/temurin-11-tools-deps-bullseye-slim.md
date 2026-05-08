## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1f43fb5576d3e10c432373f0210c89f0ce8eb295bdcebf32b32fc32030dd7905
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4ae9b1199c30d6394b7fb274b656b9a70ed2e03c6d822674b82ac4e78aa3024c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235331273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bbe7b8d60b93edba10b427c45b077242020a2bcbeb5acdb810ca3c582233fc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:06:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:06:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bf9d03800cbfdb76d6c19bf9077afa0eb28bdcff656064d9ce53d6d371bb`  
		Last Modified: Fri, 08 May 2026 00:07:18 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62733ccdf1b2b423c057fbd13b15a2477a682690fbdc68319d635596faba467e`  
		Last Modified: Fri, 08 May 2026 00:07:17 GMT  
		Size: 59.2 MB (59186503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad8f407fc15dbfadf1113eb20185a455b534a737c43da65be5fa40ef38c32cf`  
		Last Modified: Fri, 08 May 2026 00:07:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7661795259fdb1ca10e677fe45d86550d5b74b4b86137a86533f9d490b1ba22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57193744bc5c5c666eba844855a6120a13745efdef8f18317389d4252d54f879`

```dockerfile
```

-	Layers:
	-	`sha256:38784bdc94963ff919d377085a23507ede02899ad10b15ebd99ed0f65caffaa6`  
		Last Modified: Fri, 08 May 2026 00:07:14 GMT  
		Size: 5.3 MB (5340196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d815b7567606a6e81890008b4c39995023b33c7341dbc59962c00cf452082d`  
		Last Modified: Fri, 08 May 2026 00:07:13 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e42f23fe0e5154227777fea7989ec56047dfbaf909c805c89ed021e07e7c93af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230656555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab590805ccdeea27f41fa0f70aa1f8975c16899726f223f92257c1e0f16abf28`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:08:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b940a2dea035839235250ff0729470741a3a5d1f593458a8ffcb8a3df9a07`  
		Last Modified: Fri, 08 May 2026 00:09:08 GMT  
		Size: 142.6 MB (142582244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca05311ff4831327e24549116c7dd1327bd54e3c9f9f4ab2d2be073d7533e5d`  
		Last Modified: Fri, 08 May 2026 00:09:06 GMT  
		Size: 59.3 MB (59331154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3a89d17088ef9d280f05b68adc18d69779aaade35ddcf25fcd631b1b2aa7c1`  
		Last Modified: Fri, 08 May 2026 00:09:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:627864bdadf64e8bafea83e63bda750a3f0aea0aae75da99b098d2f720f54b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7017739504469352dd831ebdf6743e40a6c321f8bd12dd139b1701de6b144c02`

```dockerfile
```

-	Layers:
	-	`sha256:ff3b3b31c0d14ccc69d9f90ae8cecb921b9428534cdf34d9ffaa57074b4cf3eb`  
		Last Modified: Fri, 08 May 2026 00:09:02 GMT  
		Size: 5.3 MB (5346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c96494c107427b9b406fb8501297eac16bfc0c4d3c9c153f79c24d4f6672757f`  
		Last Modified: Fri, 08 May 2026 00:09:01 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
