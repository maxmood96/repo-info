## `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:fa721bd80e67da8a8c154dfde59fbf6f6ab8edfab76417ea436a059d6fefa6b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b5cc359a1d737b80c815272391c934645854364f06a50b8592cc6dc638f0c84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215581183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584a81d5c780c83337f3fd9e440cb0c1714b1d99124da1d5e6054a1b4e9bfdaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:25 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d4d369041d528a310da3ce638b942eaa09c57042b1fc300e52c0f5f8febb4b`  
		Last Modified: Tue, 24 Feb 2026 19:57:59 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd01b049404beff5295f60df8dc64d6dac1c84a53472d87f56cf51df44396f`  
		Last Modified: Tue, 24 Feb 2026 19:57:59 GMT  
		Size: 69.6 MB (69567419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9540a92a117db750bcb1210d5c88f29ffca86cee3f4eba5bacc71242228e94`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8aaa21456c24979c7f204272d48932c0a4bbb32ab9eecad933920dcffed31a`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e0b82f8855d005e0720e9b53c278d89613d5ad5ffabb80b4e2ab81e2c9b8c8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e940817a7dda5aaebeb47c521bd2596cd74ef9861f793b71811c0ababf65b7`

```dockerfile
```

-	Layers:
	-	`sha256:edc87a4bd2b3a20e979f6666a248f61074deb2c2700a3fd2fa5306a2d955f6cc`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 7.4 MB (7375838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42d68284df97e84d399c2c6fcc50a9dc492802cffe40eaa729c8941de2e20df`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a4a4a9cb81f08a0ec8e9f5fe32938e4874403dde5d4220989466394718a45cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213255994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec1a95d15fb5d920630fda827ab8adb6549b69281638344f5c1faf41083107b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:08:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4ad7074dc202dbfd1779f418a1e59125b36f39a6a10cb37c49704cb98f5db`  
		Last Modified: Tue, 24 Feb 2026 20:08:47 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5fecc411eab2dda56c4df14091667b40f7de01eca97e139f9afa1bac87ffaf`  
		Last Modified: Tue, 24 Feb 2026 20:08:47 GMT  
		Size: 69.7 MB (69708296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9100de18e32725f9f44f7ecafd0c187910df535f71900eb57dcd1d05f897a25`  
		Last Modified: Tue, 24 Feb 2026 20:08:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e560c848dc91d7924a1b7e32a4544677dbaf1630f9b8a692c789d1a548e1befa`  
		Last Modified: Tue, 24 Feb 2026 20:08:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:000377d0f6849d51da49b0c09596390b9663a919dab8aabb8e496adb7a94b827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09b984406335cbd59aed856e0706d7c237c43922f215da86cd99ff73cc88878`

```dockerfile
```

-	Layers:
	-	`sha256:d3a830ce6f5b84db7ccd8abdea219a80dc0ec1e2e6b247811ca0019ea3d0799c`  
		Last Modified: Tue, 24 Feb 2026 20:08:44 GMT  
		Size: 7.4 MB (7380958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1bf9931177f2b46a247fea25793290dd0519b06e052290e0764ab2b2634014f`  
		Last Modified: Tue, 24 Feb 2026 20:08:43 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
