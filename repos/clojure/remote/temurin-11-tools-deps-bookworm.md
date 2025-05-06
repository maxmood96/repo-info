## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e8e3b6fc2d6b2e353e5134df578ef8148b28195597db61be227ee1aff677409c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5506316830e286386b97f37b2a3cf4ad47f1368fa2e4f11dc052c68ebb3b3b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271592768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd380495ec81664d1d0c93c9ceb4b6db8a79245c23a900333aa11335f177eb7`
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
	-	`sha256:ea2bade2246b0e1d98e9da5b9d8577117a3ba492e98bdf4ccade6f12b08f617c`  
		Last Modified: Tue, 06 May 2025 00:23:18 GMT  
		Size: 142.4 MB (142420730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e763f3aa91b5181b304e6b549c54c92f39fd014194bfd0b2a887984a9583272`  
		Last Modified: Tue, 06 May 2025 00:28:04 GMT  
		Size: 80.8 MB (80843748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1ba2ec4b1d17757b5dd0c5ff561ef21ed3f378ee25a3b6c9713ea901be6664`  
		Last Modified: Tue, 06 May 2025 00:28:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0810baaef531b03efea1c1ffe8ef1895e68bde3d816237bb22b465acebed33c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7213368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31fddd2883c64e2783861827c517dd68fa80b0af3359efd8591560f13ea291e4`

```dockerfile
```

-	Layers:
	-	`sha256:3e0b56ca0e1643a697f1cbaf545dbd9a8c78bd7f23ac133119d1fc1153bf6b39`  
		Last Modified: Tue, 06 May 2025 00:28:02 GMT  
		Size: 7.2 MB (7198998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9d8c9061d0933c49d51825f5d11ed3682ab05d103cdaed7f9a1ba8f39a87d3`  
		Last Modified: Tue, 06 May 2025 00:28:02 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
