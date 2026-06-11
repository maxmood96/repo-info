## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:afc9be29c2e0cd1be424257201c332cb3a811f003aa2f02a1250d6ec47f677bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cda89f54b6eab7bb91445a79940963d8b7874c170f82c6af4cf2733ffdf1326a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278451857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c0b5c70bbee7275fb9febea0e25dbe73028315d6e691525584ef3c1eee5df9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:58 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f29e6cc17a677e6bfd3c971c97836d4923d855cea1bebf5975e9d7e9622eae`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab5ac39b3a480c83c665f8eedece4f90d16f9813589992968fc23d46f3f284e`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 66.5 MB (66512125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9303ba65f1877caedc437ff247d0b8c51dcb3db891f34bf506c5115586633b`  
		Last Modified: Thu, 11 Jun 2026 01:20:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b029947dacce146fae0de22303b752a9ada8a002be9309a02f9f3067ef4dff`  
		Last Modified: Thu, 11 Jun 2026 01:20:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5b6b5a574d6116f98ce5c013e9e5800fa6cd1c88f94471550ef80444ff047679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6230f8a64a2066ada510e53e0e1c81373c9422b8526db9aaf10553477b23a22`

```dockerfile
```

-	Layers:
	-	`sha256:1d68769fe31b1d43944aec0a891ada2eead2822a9e9183d90d37ce73260f4077`  
		Last Modified: Thu, 11 Jun 2026 01:20:29 GMT  
		Size: 7.4 MB (7407301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045fbd70927e5faa21b3bfab45242c7dd1fc2c6b92d599d7bf7f25281717e634`  
		Last Modified: Thu, 11 Jun 2026 01:20:29 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19eb2cbc76fc0d2c286c82e3ce811c952f1a79d4472aecef4e00e4fa44ac5986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275404041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a147977e66691953c66b79867bbe0391c537c5b2744e4579f5398f798cf54fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:14 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cf12cd0566b7e2a6a0171f19907169d761da183efb926bc6d56515a21c932f`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec560742dafd586215456dba86c488aca38c73d12af1c7b5c8b6e8bd073fdd0e`  
		Last Modified: Thu, 11 Jun 2026 01:24:51 GMT  
		Size: 66.7 MB (66677557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14a7dc081ff089025d57ff680898fb10a6b4f403189382f4bf54a33f5102e2`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de2df0406fddfc26ee9a3a19b91139ad4ab99dd33eea7a3b4d002e47056a1b`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:228ef6f0c2c1b98b381a9285ecd07fbd7db8296cb4f6e7ab99c599e2e8301101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58edc1920970a127667eead4f3897812c5365d799b4ab729d65b6d3b4fbb8e0d`

```dockerfile
```

-	Layers:
	-	`sha256:355e7d7f44610f47e9e3f5d8e30de33fbc68e1ce4691d3e6456cf780e11fc062`  
		Last Modified: Thu, 11 Jun 2026 01:24:48 GMT  
		Size: 7.4 MB (7412400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913a407dc1bcb6193bd28148fc359c503b1740158d1b967993a57191da5cd483`  
		Last Modified: Thu, 11 Jun 2026 01:24:47 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
