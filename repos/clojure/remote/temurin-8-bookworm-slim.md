## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:034500a0f1446f1c0d015c391a59f08c5cabb3cc7fa88cc6ae21b93c2cf303c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0fd7e6cebe43ae72a682f7b1d8d153bba4f7df7cda7a811ebd93d8ae8b2b4bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153108485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcfe922f9427044873667931e20db083e9e45a1f5a727481932eeb695f1c5f0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:49 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:49 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac1ed9682a4dfbe958cdcb4ab4be24aa8033356f6ae76468f2e6809ada7b8f2`  
		Last Modified: Wed, 04 Mar 2026 17:49:21 GMT  
		Size: 55.2 MB (55170111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5944e590849e9ce17959c4d717de3fd34e7827da43435e2ff7fb2552841329f`  
		Last Modified: Wed, 04 Mar 2026 17:49:21 GMT  
		Size: 69.7 MB (69701449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6cf25181daa2898adbfe3931fc1ce199bbd3265a065ca0d39bf7f5865f1fe7`  
		Last Modified: Wed, 04 Mar 2026 17:49:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3479861f26050ad137e345fd4d3ac8bc2e6ef4b8b57da2587dc7984ee50eaa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4138b095bc6cb2364f1a20d016c8037e7ead9fbd57f5e57a47b819942ca6e8`

```dockerfile
```

-	Layers:
	-	`sha256:095e1be7b362aef873e9f3042127b970abba9809c300fd187b7dfdf93b0bb78d`  
		Last Modified: Wed, 04 Mar 2026 17:49:19 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cec0cc5378f721552587b588626dc41a751f9d0ed7eb7b07800bf864da2c41e`  
		Last Modified: Wed, 04 Mar 2026 17:49:19 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:124f4530f32d8c3db50c240eb59ba6ea88546b4fa3db5e9f0bff5e5bc16ac8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152056775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdea2d9db2b0961ff815a8e00e16cc91af53f3ac8e52c84952ae745f98af2d3f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:11 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:11 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526139960d55c681727e8da6efc46a93462c8413cbceb92de08f81a07460febd`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad40617c60c94809fa7eaabb97d5aec98a8b687fa7e81ed6a419b4d310354263`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 69.7 MB (69688432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73be6f59489e01fa7078051acbd23b1eed31ed1cb4e9c242bd08714f80db8d6c`  
		Last Modified: Wed, 04 Mar 2026 17:48:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0397dd8bbea879ed9321011b14c57c6a89c86a84757b011b6c1c7957d380fc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f751cb4be4a2a2acf5cd2d008733f269081f949d9616c6679384f0b20a2e5e38`

```dockerfile
```

-	Layers:
	-	`sha256:42d75dc005db108bf427bcbb0ee333151e9d8e647e24384984d4e1429bf91598`  
		Last Modified: Wed, 04 Mar 2026 17:48:42 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f360b2c52a43517ea813be015d24850f260626716e3af7f96476ab2f8cb3e2`  
		Last Modified: Wed, 04 Mar 2026 17:48:41 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:70b39a1387567e3364760650814c93b2fb6fcbb06a7086cc2549482fe782449e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160262764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa6da14b1e41e2dfd6136543cb4df207d0dd6e13b076cbd1c95c14f14f03460`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
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
# Wed, 04 Mar 2026 17:48:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844622736b7280530505d1daae5b1b28fdf6f69cdd1eebb73868c0a0f1857cce`  
		Last Modified: Wed, 04 Mar 2026 17:49:25 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee27cae53d02236a4fd789cf4c7b3c40ba661a09f63a0689f0944967294d530`  
		Last Modified: Wed, 04 Mar 2026 17:49:26 GMT  
		Size: 75.5 MB (75533389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e31f66eccd706a8861a7053de61e6995cdc456a836e5a2a71e1c39b3677ede`  
		Last Modified: Wed, 04 Mar 2026 17:49:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f493a4701ffa9d4c5b24a70c4a66666f3b3b4c27768baa432100a54988e5fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ede729883b34295fc9e9630067992db9780c75fd498d5335e06539f81bd5cf`

```dockerfile
```

-	Layers:
	-	`sha256:7a9bb6a211d1e120112ac680045eb854ef24f255b71550fe28cb7a32543e31c0`  
		Last Modified: Wed, 04 Mar 2026 17:49:23 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa9008ffec384b6e452c558f651f4b5de033d423daf22130a98ae3ff42deaa7`  
		Last Modified: Wed, 04 Mar 2026 17:49:22 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
