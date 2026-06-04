## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:bd28d2b7a792e5d31e3a1d21935f21a657dfe380533b20320c15565eb4156786
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2b53b6d878b7cc44715686d469d7cc34876fcfc948ef6f69eee302d2aa0fc45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af747e9db1aaa9b2fe64f5dad7052f4637c391b2f239a106a5db3d63772715eb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:41:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:20 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3830e67c9fc47f25315f84191fee3b927d7a4645de82e11a1f6e27b3a785889e`  
		Last Modified: Thu, 04 Jun 2026 17:41:53 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab22920d03387e26c57dc9aa667b004e1c66fc774f5354e6a41845ec3d7c5a`  
		Last Modified: Thu, 04 Jun 2026 17:41:53 GMT  
		Size: 56.1 MB (56100427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558d999633b8c04b253bce1758554b5f2bcc2565bd3f7fa74c40afca0407ae19`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:621b6563ca4c3763f438ced8392b65c9b9f1f058b3b2e09827bbd95aa1dcb243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d88a2bf26a92b192f100dab4bca8aa99a2add747d38d28b90712ac100047ab6`

```dockerfile
```

-	Layers:
	-	`sha256:93f53b11b3be89bf6337700de1ea312e78ba4f25619657d16e8b0f210a5a9053`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 5.4 MB (5438205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555cd73b03514656c4c7c245bf3431b7d5363b7ddf97ca569f3452035d5b777c`  
		Last Modified: Thu, 04 Jun 2026 17:41:50 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a32925f128f065046793a1ebd573c5d3278878e88e66b41d84b0cc88c404795e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139284196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b77f9bd110818b29fd1603a7bebf861869088e8d4a746788370184c5f7b28b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:41:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:41:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:41:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:41:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:41:20 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:41:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:41:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:41:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945ce1ac432fed110360ba01b0a334e9fde3c351da7de87492a258d627dd6c28`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fba4ec54d897e15a4548107b4ee94b8031d1b505b9cf48b40344d8178c430e`  
		Last Modified: Thu, 04 Jun 2026 17:41:51 GMT  
		Size: 56.3 MB (56267642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42021a557bb5b4fc249533b301b8bc515f70fb772d3823e2382893a35eafc86`  
		Last Modified: Thu, 04 Jun 2026 17:41:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75ee948a7eb5339e49ab534ff149131325228cdec308706414878a6fe2d61024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a724c54e2e5f0aac7d9b3805878cb935e7efc447d4e77772696a1b07dad4cc`

```dockerfile
```

-	Layers:
	-	`sha256:3475dc68821fae6e8b9de1d8280556a06f439760f368c8d42c366e20ddbd9ce3`  
		Last Modified: Thu, 04 Jun 2026 17:41:49 GMT  
		Size: 5.4 MB (5444637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0c5302b322f821b2d06120a3d156f78685dad046fa300e6de60209a9141beb`  
		Last Modified: Thu, 04 Jun 2026 17:41:48 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
