## `clojure:tools-deps-1.12.0.1495`

```console
$ docker pull clojure@sha256:02a10d91ee87bbd250f4b558b067b243c3f6cced40e7a781e7d983f998647928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1495` - linux; amd64

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

### `clojure:tools-deps-1.12.0.1495` - unknown; unknown

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

### `clojure:tools-deps-1.12.0.1495` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:206cc1983daeae21119004ec4e00fee421565fd26e3c965a65d8af6d3e07f525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284927412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1953546bc65dfe4260db0aae59eca07383c7441be9ae2909c5e0354135c02dc`
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
	-	`sha256:3830f3f6245cfa167f19c2d8c8ab9554a513712b3d2d6fbc73a32920db0c9270`  
		Last Modified: Thu, 23 Jan 2025 02:24:23 GMT  
		Size: 155.8 MB (155793094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db52b04abaf6780e9855c6b69a11f5b3bc2c15b9b517917f35c8eb3dc930d8ec`  
		Last Modified: Thu, 23 Jan 2025 02:58:52 GMT  
		Size: 80.8 MB (80826384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f8d33f3ac37c3122faaaf5809f81f9d96a6349546425779088e90a22d5b45`  
		Last Modified: Thu, 23 Jan 2025 02:58:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec169795529bb7e97ef77ff818acc834ab359f40a54bf703a6d17a4f0346e5a`  
		Last Modified: Thu, 23 Jan 2025 02:58:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495` - unknown; unknown

```console
$ docker pull clojure@sha256:301fc5a4fb985dd01e713ec3714b400976e04ef0638373a5985e5face4e69182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6030cabbf4c8f5b42babc51b876bcedd6e6eb23ac914ace564d3d9207f490885`

```dockerfile
```

-	Layers:
	-	`sha256:1e5428f493b60ed553b809f1528e8a6f1923c3f4d371b42a5f5d98f1a959a021`  
		Last Modified: Thu, 23 Jan 2025 02:58:50 GMT  
		Size: 7.2 MB (7182017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21104c582bfa47fb7d4dad53689a41c6b1817d37a717f82139edace27d441dda`  
		Last Modified: Thu, 23 Jan 2025 02:58:50 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
