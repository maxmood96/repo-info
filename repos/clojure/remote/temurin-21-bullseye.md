## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:3c5864e68bc3f0c7a08193d09ba187e0c34f01ece9060bf8ba445f61a509e63c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1a48abbab337d993b8a1d940a04c080e84e12a579e30288fc6cc4836f8a8a7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281202192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3948f5ec6c7163019a8ffed3860d84728b350e86e38e60bdc23bbae0b9f11b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:52 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:06 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5f33bdf9f005eba28189daa5cfd2d5dc08b1d9076dd39d60793bc75ec21e28`  
		Last Modified: Mon, 09 Mar 2026 20:36:30 GMT  
		Size: 157.9 MB (157857046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4ca0d8d2f05e02302cec086ad43155791a2f079a36aae33c4d17a2669746a`  
		Last Modified: Mon, 09 Mar 2026 20:36:28 GMT  
		Size: 69.6 MB (69587669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47c1502a19f30fc97959e722c000adf48287f08ceef994696624f98a982abf2`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a20de858ae35576f95a5640c9195f7f444163fc2fa9cb48c5a74bc5da9fc16`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:11cdcd1e09486349b9cf0519ad1510b5b4dff69687880974f39dabc795494a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bea98bfac53df4f7bd454672272962c71ca6853a7fce92c7d96d7ce8afc759`

```dockerfile
```

-	Layers:
	-	`sha256:e814c00073f77e3587b26947227c85083ccd6ef1121c88f075dd42315b149ad9`  
		Last Modified: Mon, 09 Mar 2026 20:36:26 GMT  
		Size: 7.4 MB (7411129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f49bf93e9f6b2efdf835c5ffd1f0451e6ff25a62c86bf7c631a2c7940fb579`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0f044648f515d1842f280fff28d781091b4013c862f876ad5698a2d1d64419c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278120852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56c440ec769ec83e8e22a8425f8f84a7684189db1e9357db116571625a29cdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:51 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3315f6b8b9cc1d8cc6aa4f933fdc9f3b032b576cad42fa21fb4995cb57227b5`  
		Last Modified: Mon, 09 Mar 2026 20:36:28 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f8817bf28b30ccbb558227766ef6ef8295a5dc4ef74824eb82f15e245b39c`  
		Last Modified: Mon, 09 Mar 2026 20:36:27 GMT  
		Size: 69.7 MB (69728352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbea776ae315bb8a5a1e95cfef9abd6974bb7418300920263adbbddbd77a3bb7`  
		Last Modified: Mon, 09 Mar 2026 20:36:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d510d75e889e807f6c5a9d11419580e0e15dd321b9037426c5747b47bc9d5f`  
		Last Modified: Mon, 09 Mar 2026 20:36:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb58799a5e0c171d304fde409c5d349a47cdd8aeed020bfe3499bb467abf21f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbc7270da5a478e8133391b93384333c6aa8d78aa8b870f8d2d8fcfba33b7a7`

```dockerfile
```

-	Layers:
	-	`sha256:9245ae3ddfb0e1a699b3dcef2b3e30ea607cfb0926a438e22c93e49bdd01ec56`  
		Last Modified: Mon, 09 Mar 2026 20:36:24 GMT  
		Size: 7.4 MB (7416228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5aa81314c1f1925e3af0e23a36f260a0de524669ef3312f8997582c73bcb683`  
		Last Modified: Mon, 09 Mar 2026 20:36:24 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
