## `clojure:temurin-8-tools-deps-1.12.4.1612-bullseye`

```console
$ docker pull clojure@sha256:958f76604f4621c1e67230b6e1ce8c4975e454f7f2f4557eb902188e315a5eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1612-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c4839b003394c627c93a3896300278c76a624cac95584ea1d21c1fa1bf9c0504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178515108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fff9160bffa478acab62950cbc18aea4b18e21a197b917fba68bf74b4ed1c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:17 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:17 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ff83ccd996d2f3ca744a9d25820df2c919f69ece9409bc268c88f5f3551af8`  
		Last Modified: Wed, 04 Mar 2026 17:48:46 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c45fc905db0d261dc7d537b742a1b4eee83c318e96faf63c93a8de6ee98d77`  
		Last Modified: Wed, 04 Mar 2026 17:48:47 GMT  
		Size: 69.6 MB (69587911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6882f935afe095ce544c74a6df84c57f9cb828ad2c61a3695349ef3abf573c`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:075ff84f86049f524e79214194aff85a4ee3e50fff5d73f7cab7d2ce3a9ed017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7544458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfecb49e314dedcff8bf40ec5ab7307d0de80bef1c27ad5888dbc4381a808bc`

```dockerfile
```

-	Layers:
	-	`sha256:640b55860a0fee540aea5f96edb99400728898650720d152153bf8bb6c8d40b8`  
		Last Modified: Wed, 04 Mar 2026 17:48:45 GMT  
		Size: 7.5 MB (7530264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:141607827adedd0f3883a7a858745de9a328b02dec53d67e3e24d90df0f43129`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbef75d38b71da3c1a9b4f41ee11a3d80481e343c6825cfe629c0fe8e26563fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176238724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d3fec0f1ccbd8291e1e446ac10eb3f1673507fa06ed3671fd45964df1a23f2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:12 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:12 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526139960d55c681727e8da6efc46a93462c8413cbceb92de08f81a07460febd`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c00ce47c65ce9a6d2f10a498ebf9fd058ef482d37ae2f3751706b8e128a270`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 69.7 MB (69728070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fed4745938a8137ab2a66dfcb13d11d037c0067cd883e80edc6954ebc0376fb`  
		Last Modified: Wed, 04 Mar 2026 17:48:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7c6595a539debcc1335e0dd4a37f50a218c297c1358b7ac5ae184e762f39752b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7550375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aab844711dd6ab99eedf1bdbe4c0f891d8e2e7fc497649a6a5f1baaaaaae290`

```dockerfile
```

-	Layers:
	-	`sha256:52e2950494359eeeeb66d76aa8eba336f98aa13a280cec8717ab757911678f41`  
		Last Modified: Wed, 04 Mar 2026 17:48:41 GMT  
		Size: 7.5 MB (7536063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c661c326ec7bfd66f7bf148d67baa4deb2e04edf1268c1d10e8e4800623535`  
		Last Modified: Wed, 04 Mar 2026 17:48:40 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
