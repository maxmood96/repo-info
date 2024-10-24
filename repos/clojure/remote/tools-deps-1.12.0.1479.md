## `clojure:tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:50e286f6445d59f084fe72083ea5db31330b0dc10f08b5a164110d869cdca622
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:a52265103d42a3a144d13e432b2648e233fb3d8f13fd014a795c414fa2a444af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288053016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f2abe7f16c86533d56c7082e8dee8ae898175aae2c991e47c9800bd33d5033`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d60fa641d3052c24cfe2bc56634299d6b6c2d92f4b3c4378f0eda2eb8cc82b`  
		Last Modified: Thu, 24 Oct 2024 02:01:07 GMT  
		Size: 157.6 MB (157568701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca21b21a9be17918a0916a74d3a48cf7c498abf81fad76c2f41588a33a674f95`  
		Last Modified: Thu, 24 Oct 2024 02:01:06 GMT  
		Size: 80.9 MB (80928250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a919b930c5c7fe9c74c6a968c61d3232aa999dcf006b6b730533178da4725`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45e42e7877d9ff951458e143bfca75d6d81aaa9104a3efd8b3e5cff14030b45`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:624fb1f44dff857561c33a5c80c07bbba658038151a35b9cba4d7e73d6576284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff66df8581be80b075f9b0164c841dab86a3191f96ddda27b833418a1b49d5a`

```dockerfile
```

-	Layers:
	-	`sha256:ad683b2e4f48b8d6ed0f4ce302a2ac32281d281f24c603d5a43e6e8f8dd3a3cd`  
		Last Modified: Thu, 24 Oct 2024 02:01:04 GMT  
		Size: 7.2 MB (7187494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a808583dc4428aeca4bbc68d7dab127140f1a623bdbeb7b60f631b9234fd30b9`  
		Last Modified: Thu, 24 Oct 2024 02:01:03 GMT  
		Size: 17.6 KB (17646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7380e80ecc16e6c0957aa098cec1fd9cff71df841b106e718176767f2242b5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286169156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b9a198d7bf2db8a7fa1b5a3304cc5ecb96f941e3fe2eb506a93489b508d5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ea3eac04a80b5e18d7d58af963d256a6d692ad00e74729e22413155362f24`  
		Last Modified: Thu, 24 Oct 2024 08:50:34 GMT  
		Size: 155.8 MB (155793073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41f83781f4ebbef83ada558d6e1db36f91155af48ee46504889e78114bcabd9`  
		Last Modified: Thu, 24 Oct 2024 09:30:39 GMT  
		Size: 80.8 MB (80790067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b42411cd2fd64590c44fdf2fe435a23763f857c958e7bd152ce1af650348c`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3b124dbfc9e4277713bd904cf009ee8e47abc8520bcffa21635225f655db39`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:18d283e6cde338372efb214988036779f212254cf50306f57aec44dfb1048475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cfdadffbcccfa57b4ddaccdc97160bb3f806146f49be91ee4d7cf7b34e2e73`

```dockerfile
```

-	Layers:
	-	`sha256:9a0e70f0fee8432b67808d5bdca7cb9674aec7c5dfe678d927cbe4672565fc04`  
		Last Modified: Thu, 24 Oct 2024 09:30:38 GMT  
		Size: 7.2 MB (7193334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e74ef3b024266ff5dd31185a133cadd6842cc35786152b2e677bfeb1747abc9`  
		Last Modified: Thu, 24 Oct 2024 09:30:37 GMT  
		Size: 17.8 KB (17830 bytes)  
		MIME: application/vnd.in-toto+json
