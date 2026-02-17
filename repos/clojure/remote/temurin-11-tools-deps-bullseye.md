## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:415d03a6834b97c6e87c989509f4ce4d72a5ac702785ba85c0eeb4e7aea059ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:466e65f9de2abf3ce81fae400c5a998158d11492f869cd5736e6975bcc8888ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269105249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a281464f8c2794af902ff0a3bc2d04e49a8c4c799da50c893275b1d610df4587`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:05 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2596e2b48de18bd90fddddd776cb1e5f7e9ab3bd4debfca622aa8982f56072`  
		Last Modified: Tue, 17 Feb 2026 21:42:42 GMT  
		Size: 145.8 MB (145806699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a516c8e3cf47c36639bbfcdf2ea27c9e1616bad2eea03902febe08fbdbb06`  
		Last Modified: Tue, 17 Feb 2026 21:42:38 GMT  
		Size: 69.5 MB (69541644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4dac7a8a9636ba24f5c358b16f49eb78e69384ea69fd7fb7afc924e0e71ab0`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f1705e18478bb606cbe02d4e537e875c7ad61901ff9722ca6389259efc43372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ba8a459e874a71288cd31143b864cf76cc10c44b077904d5070be775b7657c`

```dockerfile
```

-	Layers:
	-	`sha256:ead25a798fb6b9bebfd223db00dc7e8c72bc489f33850908ca56ecc38001d760`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 7.4 MB (7417861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3370249531996e80b7e92fe2511f36447ae884cefc39cd03bff033e322af9fd`  
		Last Modified: Tue, 17 Feb 2026 21:42:35 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25291f05a131f78ede765e978e5b2f1b49346a0fb3ff8b705872a6516f2d62ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264453716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cffc6f943982b6691aa812cc844b8ce67e69871df40e437a0cc1339bb4eb977`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:03 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d3f6f14a6d69036f1684a692b59f8172aea6e9eaca8de9a22173c73e5bd98`  
		Last Modified: Tue, 17 Feb 2026 21:42:40 GMT  
		Size: 142.5 MB (142501432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c6d3d3df4ac87fc3b2f5096ae55fc9bd48f11bd3dbfcc7eeadda8fc0c07cf`  
		Last Modified: Tue, 17 Feb 2026 21:42:39 GMT  
		Size: 69.7 MB (69693317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b3a9fb2b7bd4d593e0ae97de600f08e04f0a68d4aa21cbdd26813582a17e81`  
		Last Modified: Tue, 17 Feb 2026 21:42:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a8c8468edac3d284d560bcebd7341e1c645f09f010e497e3f1119ed9d7c48a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebce357daaed3b01a353061239d16309e0df492be7039311d8ec522f40ea85c`

```dockerfile
```

-	Layers:
	-	`sha256:ce664ca783c53c6d8383e4919d8ead594630c70c2efdddf153ef2875bb6c5098`  
		Last Modified: Tue, 17 Feb 2026 21:42:36 GMT  
		Size: 7.4 MB (7423578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5acb3f3b7498742491e1705f660334b5b586c89349c4a97a38540c4bb6393b3`  
		Last Modified: Tue, 17 Feb 2026 21:42:36 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
