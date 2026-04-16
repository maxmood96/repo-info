## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3aa3fab2b4c54e96889f4d3234e7aa83a0da1ab259b688a4df0d740b1d902568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e1c78b11de0d1a8ba4cd496d4b6d9a2e73f1ea4d14b2dede32b97b1513d989ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247308106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf8b98209bc5fa39dd880c572e4a7a401aa34f734a87a9316ffefaf9922d5a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:05:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:34 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7630267f7564171bdcaf989c60bc746580da069489e9945be7b3136434a761`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cffe32cbcde9a6777125dccc8385773f5b919b0dfa9c3c6e7e02ec9eca1346`  
		Last Modified: Wed, 15 Apr 2026 22:06:11 GMT  
		Size: 59.2 MB (59191984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f989607a3b35a02b82791e15794d7f4bbce1384facc535535e76f553e2b890e`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c78bf30db179be7bca6702610f41c0c699ffa60d97405a07d44b0d67756cb`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52c42fe92bf8fc8f06b0f9e66e66f87b259f639058e0057ce1e388e500474144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96d8aa75ae900f59a52ef14b5183e747384d99cd7e26403d897bda9919eae92`

```dockerfile
```

-	Layers:
	-	`sha256:e287cee5e5a44591eedd046f4bf68bcd657dc1ba504908ad4e8e240efe98a7a0`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744c2c76ee7e85cba08350e425a1bc697a04a83152c26c4c977a5c4e7ca69884`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:608f92784c6ddbba3d9924c93d0eaeffb2275b5333ec0a70c960c89e2712c45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244202477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f816455248bfc5f1d84249c72e1d8d73ffc1ab462bb9c567989e449bf8d0a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:26:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:26:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662db87eb8c9c099fa996f98f4061d517bbd5dd471c0da52aa51de2c6d5746f2`  
		Last Modified: Tue, 07 Apr 2026 03:27:31 GMT  
		Size: 156.1 MB (156133049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a64e8e0f3e5d8adec204102854db8960e2c1a276a4f10eaf9f8c080e9c6de3`  
		Last Modified: Tue, 07 Apr 2026 03:27:29 GMT  
		Size: 59.3 MB (59323699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f25dd7c7c3edaf45d4df452512ba5d4d48339ebebfcec4c3a2ee8d891f2b178`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6513c8a86619a58443a5efb5b7ad8808d5f74df02343adc6c415882ce5298e4a`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e35ea43d7d60e0e0c108177cf43fc787207de2c22490fb01001a8f8cf0869f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188014cb9958a1f24efa21e084ce6069ed1a853dc405cb2a913179600bd68a6f`

```dockerfile
```

-	Layers:
	-	`sha256:1dad5411b66f68927be285799317be0c1e55194434cba98ea7a740c507fd4f6d`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 5.3 MB (5327637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962dd68f4c6c4fca5199c46011f789a838bab07a8551b217ffac3d9f123e957`  
		Last Modified: Tue, 07 Apr 2026 03:27:27 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
