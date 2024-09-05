## `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:e1a16d60c0f10b0f4978f79015badb1fe9efe15b9f910818a28ae1a9f6bbf86d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d1f951b93928e4f38a976e371b5ed16bfb5abf3eaf35b66b9a1f5e0e49850bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201766723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dfef1d6993af035d78e79f3bffac2331159d6fcd97b2b123b7ec221d803271`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085e3cb5507f2d475e154c169d28467562253bd79ab1b1bf72f81d4cdb2e70d2`  
		Last Modified: Wed, 04 Sep 2024 23:07:49 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec5d5bca970c21ca2e1dea7092666bfa0052043743459e5446ece828b9f541b`  
		Last Modified: Wed, 04 Sep 2024 23:07:48 GMT  
		Size: 69.0 MB (69027712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cca70dbb0d59adc58ccb2f90c95a6b2732155cca18f232c8a632d0220328b3`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27da3bd143aa19c33a16dd11e4be8d1f5a6166225687924a35e8c43aab54e100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d28cebd7d9fbcd6e17f2319c60195aeb28562265ec922d13bb20a2bcb5dde7`

```dockerfile
```

-	Layers:
	-	`sha256:785a36e0c9b2a5763f0f018a56234f319a88ad1edf8e9f7e8cb506525169c434`  
		Last Modified: Wed, 04 Sep 2024 23:07:47 GMT  
		Size: 4.8 MB (4770655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f807f61255ea2a2a15e2dcdbecd16e07f714e2d0da51afd6e166a505dfdc19c3`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea697214feffadcafa9b21a3687d198729eee40740827f1f1e7fc4fd0a1a9657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200659249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6debbb9706e90788023e1afe2b4084ddc26e47b122b731a2790a62c00e34240`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edcc7a7af68400eeaf570c17969676510119f264dd0e3c2e9727f01574ef515`  
		Last Modified: Sat, 17 Aug 2024 05:51:40 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3bead7a57dc0e19cb89ede2dd23bc3f99e00d3fdbc8029756ebeee42c77f26`  
		Last Modified: Sat, 17 Aug 2024 05:57:09 GMT  
		Size: 68.8 MB (68772855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac1d1084a3b9e944e3c1e469cf4fe436f24386887b751d633fc3514f45719e2`  
		Last Modified: Sat, 17 Aug 2024 05:57:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ee945ce8a19c38ddfe2df4740d2e529a46f17e119749fd84daceadb7c0bc000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4791501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce403f94581209794f4d67c6e20334b409436dfe7f7682e623dc135cd2df27`

```dockerfile
```

-	Layers:
	-	`sha256:4a2753663594de653db6f00dbaca61fd7fdc093d30cf41f127f0220649d6f953`  
		Last Modified: Fri, 23 Aug 2024 20:47:24 GMT  
		Size: 4.8 MB (4777040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569cf0cc338e7087186074ef2754e7ef19c609fbd57d4403ca963bbbc385af68`  
		Last Modified: Fri, 23 Aug 2024 20:47:24 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
