## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c6db7773583feb5ed9a4ef047d7f32b633f2aa2aa68d1ff714a2c5aa55519735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ee6521662f2de6f3cf78f07d5cb8f42debc6c46c0821a937defc563b7dd013f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181706117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157bee43ffe2e3d936d876b3a0a5d0a5094d8a40ff260bee98ccf891d7b077ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:52 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:07:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:07:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdef06cfacd6d82f15778116f9a6785af2e94519b5176f4840e2725e10263d1`  
		Last Modified: Wed, 15 Apr 2026 22:07:26 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955b169065bbd3ab10161e9bce0dda82c44cff119dd5c6906033486fbb471928`  
		Last Modified: Wed, 15 Apr 2026 22:07:25 GMT  
		Size: 59.2 MB (59190734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae95411f39c84710809b00e9200dbddb713f782e31d344889d178d6e679c432`  
		Last Modified: Wed, 15 Apr 2026 22:07:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c7d263b3a89557980a995f0d3dc6b725e43ac94fb813e4013046fc8e8fd646`  
		Last Modified: Wed, 15 Apr 2026 22:07:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7ebb1e84500dcd4f8dbf39614aae6d5bb53a943d144f8411655aeb0a1d51995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24ad1b03fde52a9440f61141c1b16e9e4146b262b99b7d10977506353013221`

```dockerfile
```

-	Layers:
	-	`sha256:d678b5eef3598210cf3377510c45d13fd5a0d4683fecdd2604728acba260bd2f`  
		Last Modified: Wed, 15 Apr 2026 22:07:22 GMT  
		Size: 5.3 MB (5288147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e86ea4db7c73c3fdf9003d48523e9d183f1afd7e6169eaf9311b3e2eaafe57`  
		Last Modified: Wed, 15 Apr 2026 22:07:22 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2dc8bf5f06a8dd90a4487a924cb88788f9a1dcf617479aa2b61b0690da28e81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179364126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e9781f0cfec74e0bb6cbf21efb617de1ba2ada93796f7dfe6dd662dfcbaf49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977def0093bf36913c4fe8dd690717359ecc3a9d68f6612b42ee9721c0d8c9a6`  
		Last Modified: Wed, 15 Apr 2026 22:19:01 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c25677d30d04a48cad429e4575eb8e5edce0b1a052382673877c2441bba1644`  
		Last Modified: Wed, 15 Apr 2026 22:18:58 GMT  
		Size: 59.3 MB (59330122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1c00df8bc6e0b671f6fa151ef0f2d03f80b16b72e9865a795a2e7846801517`  
		Last Modified: Wed, 15 Apr 2026 22:18:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dc4e62920ce20d2fd95f7c4827cdf628681d39ec325ea3da6593a25302bc83`  
		Last Modified: Wed, 15 Apr 2026 22:18:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfd9c900908254d03625d391e7bbbe07a79c850175a7af4620dd2f2dfe165d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07421aa5a6d52a332369f5d82d287fd8d5e0d394353de0865015b5f3a098340b`

```dockerfile
```

-	Layers:
	-	`sha256:5315ced4c1f05302d290a58a30ee6472681d80b69b34c993a13f9a4951670a17`  
		Last Modified: Wed, 15 Apr 2026 22:18:56 GMT  
		Size: 5.3 MB (5293900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d3fd41a397a9c9faf16cc9d02530a5a1446d922551d5f0dcd0ebeeab7b947f7`  
		Last Modified: Wed, 15 Apr 2026 22:18:55 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
