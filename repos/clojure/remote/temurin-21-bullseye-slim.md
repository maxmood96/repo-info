## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:2f997532cc71eafd7c6ca17afd212188ee13e548cfe4b1688cdfee6ca7d8f8af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ca8b1aec32ae43bafdd38e9e1a8c7833da31cd36bb2db9f003cc118328ec4cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247641168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a53be62e9bbbb91fc91bc48b438b962a87733cdddd71f10aeb11844aded4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:51 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:51 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6a87ae14dc872e5913137244bc799426bfd88b1fb56d03ddd55fd3677efcb`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88123002fe47d6621a7136caa83eee35fc7dc72c397cd8ae19fd148b12c2a47b`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 59.2 MB (59215227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5b46a9da270dbf90a200f36e1039a5b8aadc5a808ed0fb1a5f1fd1a20962c4`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f1d7d7fdc8476de9e21e6c38ee7a1e0c255b24d93cdb12033263ed8669ebe`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b01edf35b510c1fcff0b17dee20f9f6e04193ba24f1356212c4b636e87e537b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d5c6bd8bbee0861b5e9c2693b7480f1b0cd5233c12816d6d0dcad6158d25c6`

```dockerfile
```

-	Layers:
	-	`sha256:132578cabe0713749571d13c537f32b5c25448bb56f0c01945052b1f3740461f`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 5.3 MB (5322530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e52e5aa5ddf504e6f78a13b73d7f8f253242bfbd774f790a31161b34c01e0ff`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb25ca1c60e29eed90afc1de0b0be3ae6a6a6a2423c243a52bd787e626cc164a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244563161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcb4daa7c903963ba94ff2d32ffb319ceb76ae079f3508812f06cfafc915c53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943c19b4afd70417c9c5ec522c9c9116999a9a62470e556df6f7870613d6ad5d`  
		Last Modified: Thu, 14 May 2026 23:36:28 GMT  
		Size: 156.5 MB (156461249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e8a67a67d37793513485b828886eadffcdcb6bfc486363108b89e675f00bc6`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 59.4 MB (59358278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5b46a9da270dbf90a200f36e1039a5b8aadc5a808ed0fb1a5f1fd1a20962c4`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f1d7d7fdc8476de9e21e6c38ee7a1e0c255b24d93cdb12033263ed8669ebe`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f432bf298e5350a4cc66a51c61d5467e4fb3407ae7fd47f1794567e21a07bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6287b022469541eff7923a6adbe334fca660b5ee97a87ba1a9b0be3e72f3dd`

```dockerfile
```

-	Layers:
	-	`sha256:b507bbd82d7aeaaf16057ad3270e49cb0791624067151f064d231892c7201796`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 5.3 MB (5328262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4968279e23693ebffb38b0924669c62190e7dd318ba4f96ab74f925e4400c769`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 16.1 KB (16107 bytes)  
		MIME: application/vnd.in-toto+json
