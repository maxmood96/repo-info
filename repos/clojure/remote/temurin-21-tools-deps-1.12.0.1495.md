## `clojure:temurin-21-tools-deps-1.12.0.1495`

```console
$ docker pull clojure@sha256:e1ca53afd4891691b2af31936ec421e67ac78920aaff054ee8589cae85d24f1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1495` - linux; amd64

```console
$ docker pull clojure@sha256:534bacbd3b430a0f0a15744b364a993c9d1f6de9115dfbc1ae357464d681fb2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287027600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965372de61e732594f2848e9d971251b0e7d5af9e789b1b43dca03ae3c2682f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11531082a7acaf79adf0d9df474cc78ef4b359bb9b3941e8f47c7ae668e227df`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 157.6 MB (157568695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1e7d6e40edf119b03ade282766f018937ac58d69f93fd25e9ae921d549a9df`  
		Last Modified: Wed, 22 Jan 2025 19:37:08 GMT  
		Size: 81.0 MB (80977901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e476f51208254c631a7da4db98f931d444c4146f908481fc48091aeb9e7d65f5`  
		Last Modified: Wed, 22 Jan 2025 19:37:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5098acec74ba7ea02eadb9ddd5eae308d6a3bd3ec3642c0c805fc39093b512`  
		Last Modified: Wed, 22 Jan 2025 19:37:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1495` - unknown; unknown

```console
$ docker pull clojure@sha256:1b2f90ede25010dc1b08cd09a9977b6a1859c5845520faadea3b244aa6be37eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9495db6d3b81bc2fa5492bf15e3cc3d89a71d21f8d01016c7fb3d99ca2f0d7`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1355ed35606db07bce108e992e0e81cddbb25a3a96e92c958ec16e3885270`  
		Last Modified: Wed, 22 Jan 2025 19:37:07 GMT  
		Size: 7.2 MB (7176182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80618a5a3b5df9bf89cb5b253950cb73592174fff3aac8002c2b63df3a157765`  
		Last Modified: Wed, 22 Jan 2025 19:37:06 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1495` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:305cd06cfa8022b56851e15ca5cf701d1f4151681d270d56cbacb0a9b3257a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284926127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545ecf8f1b283d6e42b80363853aaee1955aff9ebe282517ab6f3ee30026ebca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea4c7f99894f5528b30815f43e73b05444422696f22795919e799360d6320ce`  
		Last Modified: Tue, 14 Jan 2025 12:12:25 GMT  
		Size: 155.8 MB (155793154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db2af42e15c0415b6ce7f8625f6e38d153cf684cc798703e40d4de86db7308e`  
		Last Modified: Tue, 14 Jan 2025 13:07:52 GMT  
		Size: 80.8 MB (80825037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127e2f7bdeab1ab8b30167d718ec148fc1b3b1180cbf4ba7a7c3195b06204e3`  
		Last Modified: Tue, 14 Jan 2025 13:07:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c45aa17a272c001369d3ec411472e9d01160103ac72f70f9d051b4a74e3a35`  
		Last Modified: Tue, 14 Jan 2025 13:07:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1495` - unknown; unknown

```console
$ docker pull clojure@sha256:22f4aab959d2ed596ccbcae14fbe4228b508ed40899a657348a4d5fb2f538f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5730e6367c0fc981067b8a64ea29c7997655132347facc38311dec1731ef4c3`

```dockerfile
```

-	Layers:
	-	`sha256:47775e6f46ae8eb373f685a10af3ab390dbc68269123118aa5ae97cb1b0a7d83`  
		Last Modified: Tue, 14 Jan 2025 13:07:50 GMT  
		Size: 7.2 MB (7182017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465461113d5ecfd42ad4dda352cce45bfe2a32662228a88c83b3851d2fd35616`  
		Last Modified: Tue, 14 Jan 2025 13:07:49 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
