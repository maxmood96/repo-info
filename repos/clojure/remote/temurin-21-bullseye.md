## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:44dd8134da40fa4898a249f311d0a1ddb8755df3be3cd823278d452f77fac3e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d91404c43864ef44b056b3da2f130c8f9b15478526e6a6d4798dfb7ff8adb7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281202752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2686b9bec18785b77d428ce4bfbbb6a4ff416b44aacc880e5fecbca25e1162d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:52 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:52 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4deeb97a8faf7c7d80e508166ee00923e84c591d4860e6bd3c64b928b57feae0`  
		Last Modified: Wed, 04 Mar 2026 17:51:35 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012b753514ce804ecdce6e64906fb16d9fd9236d9279439f300dabecaa1a7a7`  
		Last Modified: Wed, 04 Mar 2026 17:51:28 GMT  
		Size: 69.6 MB (69588173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71546652a0b32ebe552f5944dca150befe5aa6a1f93e07eaa79305470cb7c4`  
		Last Modified: Wed, 04 Mar 2026 17:51:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eec0c3b0efd25188d8bdddcc16d6b25681e4d27416763f2053e48bb7da0584f`  
		Last Modified: Wed, 04 Mar 2026 17:51:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4e3e84987e62baefad0aabf4584e2589c0be695f466bfd7aec918803896b4e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fb3d4875dbc452ecf0895ce2c5aec381985a5cb0708b318e9b1e5657ac3c9e`

```dockerfile
```

-	Layers:
	-	`sha256:8fb68ad544b1f10ef4273c8a5cbbdd6ce95dd1339f8f56552ab906f38340b669`  
		Last Modified: Wed, 04 Mar 2026 17:51:25 GMT  
		Size: 7.4 MB (7411129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16543ab39308dcac0a7e372cc74778393c9d17c962c3a3ac8fe837e28a8c5731`  
		Last Modified: Wed, 04 Mar 2026 17:51:25 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edf9933fb68ea7c2774cf080165f176d0d6e81f4a2375da51cfd9f1d4a053ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278120308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfa2df190c95f499983e54fa239bbf90fb8594b05b2a2d536fa955a1ded0d5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:30 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:30 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d9033f5696fc4444444785f9a9fd3d47bfe3ac85d8526642dd42125085225f`  
		Last Modified: Wed, 04 Mar 2026 17:51:07 GMT  
		Size: 156.1 MB (156133015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a140b012ac8d9216047e8540411009fa9fc8e21786fc77933c7460715daab`  
		Last Modified: Wed, 04 Mar 2026 17:51:06 GMT  
		Size: 69.7 MB (69727857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299b9e2655917b021067aa258d0b347d5a70e5af1e05b6a9259d67367c7751b1`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5016abd585836759ee518545920f35ce177e2b1d577808558a067394f332bdd7`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3829d68b58b4ab15d5fbb233467a43811a503fbea00fb5bd3f6fbdcf8d0c8c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a746709ad175739310dc5feceea14317765eb7d8a58f24985d988451a236877`

```dockerfile
```

-	Layers:
	-	`sha256:ce12f1b09cbec5839931ce9e4637ba3055da9a04e2497c0451ffafea358235ce`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 7.4 MB (7416228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfc2e7801a38907fcdb140b78770cff7387291c7d8e92f46924c179f9bf98ef`  
		Last Modified: Wed, 04 Mar 2026 17:51:03 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
