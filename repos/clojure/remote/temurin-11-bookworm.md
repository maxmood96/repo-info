## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:0061d583dbe6dbf0b2ce51e9ba8426ab6edf46dc98531483b3b47af0b2724c85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:553347a20ed61eb624b0e52202fe4da15e520bf1d61334820d516ad56fd9e188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276033766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7974bb2625b4d1fb167ed95293a05fd4268717bf551e8671d2775d5751647d59`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c0ed60345efd5ceced6ad3328a65257bd0b6cfdd2121ecd54a2432036317b`  
		Last Modified: Thu, 17 Oct 2024 01:13:29 GMT  
		Size: 145.5 MB (145549908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8141f415b6b8d21bfdd5fcfe316d301aebb4b829bcca87358fd4a94060e946d7`  
		Last Modified: Thu, 17 Oct 2024 01:13:32 GMT  
		Size: 80.9 MB (80928191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a0946ec96f70a4498251164161e075d8747a0e870ab7dc13ca6b4d3a9af514`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70060bec91bb6f35013af0eefd50dce76acd6cc6b2d6d2a50b8a14186aa92bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7190716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a224e88c8b0821a1497d39f2f086e09f8f2afa6fd78326e04a7062ae0e0169`

```dockerfile
```

-	Layers:
	-	`sha256:1238265397785b18ff6ba55e53a00312fe20e3c1a3d2c3a22e0b419f011dd6e1`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 7.2 MB (7176813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bb43c6e6b9dc675b9d7b22c266b4a8cde71751005d88e6f7f1f968038e9908`  
		Last Modified: Thu, 17 Oct 2024 01:13:30 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22794abf9850dc42cf087e7a4caa7132523e63afbfc4a5caed6425500c26e046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272732445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c7815208d8c1accd8d1528c55ec5c45fd6d70486bc053cb061bf037d3a2abc`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37fe4b3f26ea0b745d94ce1fca7f6c7322f18dbef079c4b027c82bbfb40ef1e`  
		Last Modified: Thu, 17 Oct 2024 08:03:37 GMT  
		Size: 142.4 MB (142356628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8601882a8e10f052cc2d2dbfcea8fb0ce24e7411f6150418037c9ca0ce9f49`  
		Last Modified: Thu, 17 Oct 2024 08:07:48 GMT  
		Size: 80.8 MB (80790196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7296890fe087c49c3313d089e89bb58fdb911a598c0c5c44d999810a5e8e5705`  
		Last Modified: Thu, 17 Oct 2024 08:07:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d7b7e4502d190c9ba90596b714d1ecbf9a0380972b3283b43ff96d8a8400948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a4dfbb8815e8687678070a179cc8245af9db1294a2ee9e011c8a30c4ad60e`

```dockerfile
```

-	Layers:
	-	`sha256:1103d1d01d58f9f32ea235b06937ae0bd7a2a6580d77858ed485e85b5a4f0618`  
		Last Modified: Thu, 17 Oct 2024 08:07:47 GMT  
		Size: 7.2 MB (7183200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06584a670674ebd3b133fad108f25fae9979fe85590de0978397b71c5cad7ab5`  
		Last Modified: Thu, 17 Oct 2024 08:07:46 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json
