## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f9e78027402f0232fb2dd404c75360f3f1a8f03385ca8e7ad5f45b62026fae29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0383d2cf3394bc9e4a2b23aadfc85f4c352817b6a8944d5528bf8e01158c6150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215352865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee844b6a267d6ac1365d91bcce90626b23aad868157afe08534abbf3f60152`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910342737b2a9c7cd5f19aefe067e9995987b73b263ccf5a3927a756af42ea95`  
		Last Modified: Tue, 30 Sep 2025 00:57:12 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0f639583bbad9db683d451a2a3bb104775ec2e9f40d0693456f64d2fe9cb0`  
		Last Modified: Tue, 30 Sep 2025 00:57:12 GMT  
		Size: 69.6 MB (69559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72dcfa482d985725aa28a59ffb8170e464e9c87dbc34b6c61d67c4846617272`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036666dff72f40c1ea01b185fe11d1098eae0fd76f14c77bfa582d05a185a120`  
		Last Modified: Tue, 30 Sep 2025 00:57:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dadf242f437e5c477c9fe250cdda8443090a6beb3d4026a6705e84ff847034f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200826a9869bc84530f74345895afa6dcd185729e4ca0c174e8d50e5e45f66fa`

```dockerfile
```

-	Layers:
	-	`sha256:6252b679764d7dec3371458be066bdaec0bc471db690ff73596233e92e0bfcb5`  
		Last Modified: Wed, 01 Oct 2025 15:41:35 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558d20174a7bce0c50d52b21cf8d778daf071e5b73c05e6727ba1d41e8b9f22c`  
		Last Modified: Wed, 01 Oct 2025 15:41:36 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8bbc1a9a8671198c00286554089be908cf5d2bf6ea35dddd732ed9535046d005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212990837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b817587b4e1950f12b58391bfceb2ab5aa8a1b7bfbecc02bd0b119172369e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b3952b6db71cb3d2a1ebe733bd368c454ea741834896690e6ebc87b685453`  
		Last Modified: Tue, 30 Sep 2025 00:55:34 GMT  
		Size: 91.0 MB (91045212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5f9fd693775bd686c1643cd1ac0d30e8f517e144c5def603a4e8cd8f6cad1b`  
		Last Modified: Tue, 30 Sep 2025 00:56:15 GMT  
		Size: 69.7 MB (69687172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ffe49b43f91502fb69354cbeec4531494bd84774c2411e786e28e450e6d9ad`  
		Last Modified: Tue, 30 Sep 2025 00:56:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd1195f89291f0b3d4f53908ae390f2945b8c178fcc0924c130db9b39d2f849`  
		Last Modified: Tue, 30 Sep 2025 00:56:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:48337105e507488ca1391fe49170b207f968f53f2ab5f67cae57f1f40d68d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1200b89bcfbf181bfb0c14bf83a7324a1c631973332681742726a66a344ee0f0`

```dockerfile
```

-	Layers:
	-	`sha256:d190c1aa1eaf6f693fff2321aaa0206517c09b54ae284eb20f96529ba25d4e13`  
		Last Modified: Wed, 01 Oct 2025 21:44:46 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc99ae9344dcd2329c13eab25af518dc1adedb2a34f34429bcbd4469470f70b`  
		Last Modified: Wed, 01 Oct 2025 21:44:47 GMT  
		Size: 16.6 KB (16631 bytes)  
		MIME: application/vnd.in-toto+json
