## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d0061c1dfdd1949c32f6511b788d5d6aae7c8103df80577d87ed0d970bab8820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:233c12dc9f8093b27946476a4855887b6cea32bc44e8ad538eb2833ad487bdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215344535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6700059e83c5a5b4a61c18c40e4f2e9d1c735c5ee6f542990da2e638eac05839`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313df266dc596eb3d9212c601e983de8891389bde4e9941d074eb416f94475a8`  
		Last Modified: Wed, 28 Jan 2026 18:07:19 GMT  
		Size: 92.0 MB (92045288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b6248ef0264526657651a85a35dee011d6cfd2240ea77006498889d47f7f8`  
		Last Modified: Wed, 28 Jan 2026 18:07:19 GMT  
		Size: 69.5 MB (69541759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5df25c35151457d7c982c2c57c56225076a26e46cb652b512d3471cccf652`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b270a9fb9e4b0f592a43a52d42ef3f3213baaaf898e1fbc7362b7c1cfc7db7`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2e4ab7fc21db82a24d1ffaa27ac55b7f33ae5d2ee5dfc447b1d365e65ea600aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e69839defb74f35388dd3561ff02ddc67856c79a3a7aef9138e133345f76a8`

```dockerfile
```

-	Layers:
	-	`sha256:957baca359e05d6ba4e75f7e207a28a067c42c3ad27d8f4baa750b3ad32d1fdb`  
		Last Modified: Wed, 28 Jan 2026 18:07:16 GMT  
		Size: 7.3 MB (7347806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b72a0555caf326435a42ed4b1cb748a38b9c9c77a0cb160e5a44d60625b027`  
		Last Modified: Wed, 28 Jan 2026 18:07:15 GMT  
		Size: 16.4 KB (16445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f58c1b2837022a8efe07ff987c875fcace70ac85d58d09d79241a9b7ba42c725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213004508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c560e7a3024324a9731d2c70f14c4fb9f19e44e8c9a5b2281239c8755d9b140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:22 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7bed2ea4dd2853df75e6f7b73ef2b107d4f43de151de10d4241b39f537d0de`  
		Last Modified: Wed, 28 Jan 2026 18:06:57 GMT  
		Size: 91.1 MB (91052493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6834347a771aa5bd453fdfd16e11fa45d51549198d1b299d06d700bcf593f9`  
		Last Modified: Wed, 28 Jan 2026 18:07:00 GMT  
		Size: 69.7 MB (69693206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ae471303774a93dcd9ea339a970ef50c1623d6256c99891394c1ba0b8dc19`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd4d1bede5c5fc709678d62618f221aacbea73e298be4be375866e981cff4a`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0c8c4b5fd1bd63514b68d28bc46e6741f9e7f81e8800f7bcc1b300965c95969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68648e20d2903ebd9fc826f96a0ae152ab3bb9938bd6d1ac5c34f9f813ed41f7`

```dockerfile
```

-	Layers:
	-	`sha256:fc2f57cc69ef646f71fc89f10e7355a7a6d357d19646a3ea4d92a7a90f11d928`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 7.4 MB (7352926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2ebe55412d704900519cd05aa1ced558059a9ff15f4a1956965a9a79eb6b91`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
