## `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye`

```console
$ docker pull clojure@sha256:869a0a66d72ae2d15e116ef430bb30db399489c5cdf78e900d04b37958395318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2e404e2fc57d8f1f8af65b110c827adafe08c5db24b774489b38eb698ee7bb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269271899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f025533cd22009820117865e0015543979d50aca2957cda85c425c682ff3eec6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:14:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacff9c69399d465a98a5a5a539eb70f018d7fc2dd9e59ba580682b6057c1b`  
		Last Modified: Fri, 15 May 2026 20:15:18 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b755a73623bf9a3ee4191b6b2ba2beab9f25de3989c8bb9a323ed5d3bdb4c90f`  
		Last Modified: Fri, 15 May 2026 20:15:16 GMT  
		Size: 69.6 MB (69602067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3366f9f4ee5fe00ed510b2e2ab7c10fbfad17c2e16be895938bdfaeba0eeb29`  
		Last Modified: Fri, 15 May 2026 20:15:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b886dbd4e6a9a3c177026683884e8283b2e32c54e2208a6827abf30cdc435`  
		Last Modified: Fri, 15 May 2026 20:15:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:61aa0a4c42803954f04c92d3c7d96327b545c8f3be42584d196d71ff00379f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02de627cc0cdb98222734c326656ce2f00527d16e6db41c70ebc5cb88ceeb9af`

```dockerfile
```

-	Layers:
	-	`sha256:b4e618ad020b11bc0336445627c9749de895915e7165bc797a21154d02d01d66`  
		Last Modified: Fri, 15 May 2026 20:15:13 GMT  
		Size: 7.4 MB (7408278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d40e85d1ea606551a3470a4479d8438f6561404e2981782f9622dbb2eea9e9b`  
		Last Modified: Fri, 15 May 2026 20:15:12 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d448afc1b2c9b693ade9b0c430ad0193cbb76d694a8bf2a313920b00827f3454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266749464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3befd6514100d8f5e51654ffb590c927b368bc1a4e79e380ea1de8ed397c7ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:14:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:30 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:14:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:14:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22a0bc87ba4b85d2d6904d127199c53b94bd460d0088d4540cf490f5aad70ea`  
		Last Modified: Fri, 15 May 2026 20:15:09 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125a40292343750ec1ae6ab5b15b546e520e8ecaec4cdbb7f4952ff4c25cd0d`  
		Last Modified: Fri, 15 May 2026 20:15:07 GMT  
		Size: 69.8 MB (69770874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48eb6fe78d536e73e0620f506c78e930a88195a95eba27d8a2d48fafe8e9105`  
		Last Modified: Fri, 15 May 2026 20:15:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e837d4f3e547ca186961426edd5163a3f52d9d986eeeac5fbed82ea6b500e51a`  
		Last Modified: Fri, 15 May 2026 20:15:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5549dfcfe356f0dfa0ab6776f18d20c79b68f6646509a151efcb11871d13035f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f0b653f4f78c12f9c2a3de3f8c30285688e5e605a8b853932a1c84b8b7eda3`

```dockerfile
```

-	Layers:
	-	`sha256:e4219fe0bb7f936abd3e8852a1cfa9e7bc123320d6e12d653ce3b372d5298cd4`  
		Last Modified: Fri, 15 May 2026 20:15:03 GMT  
		Size: 7.4 MB (7413377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d973d270d04461ad6d5c0826588ba16d9af1ecf1d746a5563b3fbbb41c74ed1`  
		Last Modified: Fri, 15 May 2026 20:15:02 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
