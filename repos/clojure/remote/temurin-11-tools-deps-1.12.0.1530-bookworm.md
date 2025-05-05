## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:a81514580b3735f538702d56a6fd29b8208751c36fb8911eb05ed3955077d60f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2c6525fc13715697b9f939a369d3580372a79864737edeabbc54a6249dbb9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275119438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6f19109e3eca7442b15abd9b54c7ecaa6adad5c1e87803e9f75a87ac73e3d5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631e40d3b2a15337894c5d35e35eb69ee7f8d61abe127602610f8c49ad4221e7`  
		Last Modified: Mon, 05 May 2025 17:07:14 GMT  
		Size: 145.6 MB (145635734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecc2b69cd58c7ae31e128a07112cdca1d3cabf2cccda91d216ccd648cd48ec7`  
		Last Modified: Mon, 05 May 2025 17:07:13 GMT  
		Size: 81.0 MB (80991860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979388488f5088dcf5ac343ee7ca10d1d1cda5786de9bd3fc7b71f1b11439a84`  
		Last Modified: Mon, 05 May 2025 17:07:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:efe22aad9ebe5a008ce7e432daa36fa18d9a8f38d6fc88a782bb17420457f0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7576cdfa53f8574902ee3f15747393510b1a64febffebdaa97653cab048e1c86`

```dockerfile
```

-	Layers:
	-	`sha256:ca51f18cf98374463734904a5fbad118528bdc84e0cd35548e613b427545e52e`  
		Last Modified: Mon, 05 May 2025 17:07:12 GMT  
		Size: 7.2 MB (7192617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc11c66054f8d9682b904888b08fc8c227631d6f4f936a0a16e75a46d2f71247`  
		Last Modified: Mon, 05 May 2025 17:07:12 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:937579c2c624f1b700fcbf099d17775d21c883901969c4739ae396f753daa6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271594001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462b1e2edb51468d54963bfbac52747a2f6868ac9a6de3915b4785c942195b96`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4880fb24b138da8e002192f01f7a329ef7487d6d141fd140912014b9177855f1`  
		Last Modified: Wed, 30 Apr 2025 01:04:29 GMT  
		Size: 142.4 MB (142422074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66fb49c6891e37ee55f7b3ae3fc6a0a124f131ab4c19cdd1ae2d2d85acbc83c`  
		Last Modified: Wed, 30 Apr 2025 01:07:39 GMT  
		Size: 80.8 MB (80843636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d390d9e3bf9bed73f6731d496ae5d17101ae46569cbc70eaa73500879a09ac73`  
		Last Modified: Wed, 30 Apr 2025 01:07:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6853694d876f96aa4157f190d69b08af9043aff8f78bb36420882782b6fb590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328eb6d768070d2454db4b3f0ebdc5470220cf7e39dee2b6ead5b353eaa596e`

```dockerfile
```

-	Layers:
	-	`sha256:6bea15b7c28b8d708b92798538b70dbd2314a3aa1c4dd7b55ce585486613dcb6`  
		Last Modified: Wed, 30 Apr 2025 01:07:37 GMT  
		Size: 7.2 MB (7198998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c599dce3e0b5f75a8ca26e79a0e7c05cacdfa719d475a25db4960438d836cc7`  
		Last Modified: Wed, 30 Apr 2025 01:07:36 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
