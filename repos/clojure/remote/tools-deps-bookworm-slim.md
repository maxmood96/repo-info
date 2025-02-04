## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:26e58a5d25e7786f746817fd4290585499693b3eb5b613bdfb681cdaa422f323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d7374f5c6b26592f5e84c77125764e32a1a90c39059446271fa7762eef6b3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255330282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc062e0c3838a1ed082b57cdbdccaea4f2eab827de80601b0d3a65514a4ffffd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f5defcd34342522f5d8961283ec8f0f12bfd845c282831c5e1d3b4ac3a8d83`  
		Last Modified: Tue, 04 Feb 2025 05:21:39 GMT  
		Size: 157.6 MB (157585921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae3c5189e59404afa9895479a00149052580c980b75504b149fe4e8c8871ba9`  
		Last Modified: Tue, 04 Feb 2025 05:21:37 GMT  
		Size: 69.5 MB (69531020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50af7b402f682a909cd6ff268491118b33be65eaa83b77d15c3ee1d7db718f8d`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9563d06f42f6b359c55f6997d593315c1b4d7723509c0462ffd9cc751cdb2c`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09f76455cd8fe24a5605b1a2dae8988cff391e709d522314fc51e24c9ac754f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbc8a31f9ee3944fc45abe33261fa824dfa3763b952b0bba7e68d3937b18a2d`

```dockerfile
```

-	Layers:
	-	`sha256:d4bc79a65eefb6a7c4fe86ddd6b65520889afa0ddaf5444c4c10077ec32e53b3`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 4.9 MB (4916365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28dc0df58a2f6043c6fd72131502d9dc6dcd5ebd7cef03d98fcdf2565af5bed5`  
		Last Modified: Tue, 04 Feb 2025 05:21:35 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:398d32c1e3b046765b2a9999bb1cab6aa2053e2df44a7a9e3267986f0e62e90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253282961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0275db2a420a54aa011a7d53be4d7e59cd2169e5279ddc51133975b8a83df12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1941c697535fcd933d9c45096e4befd9c237b71ed44c19c94f024567caa09845`  
		Last Modified: Fri, 31 Jan 2025 05:20:04 GMT  
		Size: 155.9 MB (155859317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c9ee9e1b4d5687184aa6f9cfae92846bcdcd8eac3254bc96ca43b45de9188e`  
		Last Modified: Fri, 31 Jan 2025 05:24:58 GMT  
		Size: 69.4 MB (69381573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d6a752ba25d8d3ad8ffa1a78699595d08463a26115886e445b399abfdcd5e`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dcf026db8192a72d1f409b6174e738a67e99dfc033857b52475f380d681589`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d32e48a214622fa33f545cea3d066d8b1ed62307fe9678f18affffcdeba9eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc18ef9d46799f705a1d47ac2fe842a04a3ab41b7c12a0b49bdbd7f8ebc3b5d9`

```dockerfile
```

-	Layers:
	-	`sha256:d059c2101974007bcb29887d076294ba63552536185837a3f5d1bb4aacd32d18`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 4.9 MB (4922150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebb7463e6bd4aa5940f9ce5cd612c01b578380b46206d4d2e3bda7d285ca4ef`  
		Last Modified: Fri, 31 Jan 2025 05:24:56 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
