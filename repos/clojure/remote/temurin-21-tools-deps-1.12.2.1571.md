## `clojure:temurin-21-tools-deps-1.12.2.1571`

```console
$ docker pull clojure@sha256:6f824bbd0c2bdca44aaa8ed94590492eff3986df0bb87836088b9d0220974ce8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1571` - linux; amd64

```console
$ docker pull clojure@sha256:0b9b5930584c734b3f160901a42d21d7ba05e7c1f58e714c4ef423249cd69a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287427657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837bd84df9eb39e27966be4e437659743593afa5b22f78a83778ecadcab5744c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797d6c8561285314bb2f974198823feb702d76943e543a4e7bea07db1c8fffad`  
		Last Modified: Tue, 23 Sep 2025 01:02:14 GMT  
		Size: 157.8 MB (157804727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45bda17cec848dbae4daa6d482c11ac4c5eaf3003510c50e4593869865fcd06`  
		Last Modified: Mon, 22 Sep 2025 23:46:23 GMT  
		Size: 81.1 MB (81141279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c28dde8dc7c7c989ff47ba3e354f5761042869e38bd0089f4dce8961bcae25`  
		Last Modified: Mon, 22 Sep 2025 23:46:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa77d07a3bf431b561798c0eea74d2892393fda59eb3afff889ad3a1521d584`  
		Last Modified: Mon, 22 Sep 2025 23:46:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:407059eee352a9b0309e07b66bee32f1dc3edacdacc124aadd422130b54ad003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881be13d693923e590adab7ec66ee3bc3f11dc2428e6cb1045b99750bc37e6d`

```dockerfile
```

-	Layers:
	-	`sha256:f96b4fbf3b69d66dd493ebd4802ea502736cbfd1e44c151e2c7610860b87a1f6`  
		Last Modified: Tue, 23 Sep 2025 00:40:53 GMT  
		Size: 7.4 MB (7379992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507874fae65a1737001cefb0714dcd1f1e95370596123715b7d9f5492ba7e2af`  
		Last Modified: Tue, 23 Sep 2025 00:40:54 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1571` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7de5485977b687c58020f64edeae3f5817969524359eceb8596b132cb21b7ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285472258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f341fc235d0f7688ca55954c282fe66b499d69b66d41165970daf8f5bde7019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730c9bc7819b9fd632877a94b6339ce91c6cae9fbd44abb3f55397896408c4b`  
		Last Modified: Tue, 23 Sep 2025 01:02:44 GMT  
		Size: 156.1 MB (156081185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c15c157ea4b7eed01f11b6ac9dbbf879a908bfc82724f0cdd660ea49006ac6`  
		Last Modified: Tue, 23 Sep 2025 01:02:52 GMT  
		Size: 81.0 MB (81031010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b400ebcd214f8e24e862f40cbfebca6063a15f35fad47e5541c872ef2ff5b`  
		Last Modified: Mon, 22 Sep 2025 23:10:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0472ce879771dffe6d3a5766b1bc5ddd0a96f65345f2838161b9dfd1822b778d`  
		Last Modified: Mon, 22 Sep 2025 23:10:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:35b45165b6be3122ae5307464d776fd774c099665976337b7a6a7006d32bcf3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbbf5d6e6ca78f58a3528b8ea6d679fbfc4d45698142d0c94c814716ce8ad97`

```dockerfile
```

-	Layers:
	-	`sha256:c102b9e39ecfb1b978e379748f2a9c037849a55fbbe61b0e915299a0d634a307`  
		Last Modified: Tue, 23 Sep 2025 00:41:15 GMT  
		Size: 7.4 MB (7385827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121e752b925845b09ffc8ba0c0eb5121a3d15f39f5cea001e5a1196b436c3cb7`  
		Last Modified: Tue, 23 Sep 2025 00:41:16 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1571` - linux; ppc64le

```console
$ docker pull clojure@sha256:6b120a868f27cb43295c6d18896afafd1c670a28c56e2709d44a358622f4e8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297274441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7030e966b88e92fff825289c178f943cfcda56cb637e6cb58e77e4f576bbcc33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7184167a1ccb74bab25fb1bb1f9e10333e2a52ed41eb7b8b230fc0366b6770c4`  
		Last Modified: Tue, 23 Sep 2025 02:02:04 GMT  
		Size: 87.0 MB (86983098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d697f690a41f6456c52a50147107b64f828e88489d7e44a26a365aba541b2da`  
		Last Modified: Mon, 22 Sep 2025 23:45:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47dfabb70ec940d4cd8f97f1625feef28aa4af1a0d6d2f05298cef423614722`  
		Last Modified: Mon, 22 Sep 2025 23:45:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:5b881630672226f5a4f04b2ab2045ddf5b39cdc6ec5121e0420df03c4163f251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b354096aeddc3bdaa373c48d8e8a3678918721a156d3b873d96304077532b7e7`

```dockerfile
```

-	Layers:
	-	`sha256:030952c32bb56a5ad4d8dc7550166aca16006d1a187e6e9a6c1d8839e6737429`  
		Last Modified: Tue, 23 Sep 2025 00:41:23 GMT  
		Size: 7.4 MB (7385242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbfcffefad6457a52f19b343f180676238de71c08c507ceb587ecb95d9cfd40`  
		Last Modified: Tue, 23 Sep 2025 00:41:23 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1571` - linux; s390x

```console
$ docker pull clojure@sha256:46cee1dd333a7a4d26b019fc631c684e2628f84d6df92eb57dc72d43b525ea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274123413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aab89f43c6bea724f44051ec6cc2e37337e32b838d6b4e9954e890a6401b1ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76f7aff1b611302e68346f0ffb976ff193de7acaf02b41bd016c3ece7f590bf`  
		Last Modified: Mon, 22 Sep 2025 23:13:19 GMT  
		Size: 80.0 MB (79957789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4add8d8ff95014e394895bc7b92572a0e068c9f6674e437b831b994c8f6f3b76`  
		Last Modified: Mon, 22 Sep 2025 23:12:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bad2ea491d59c69565314171a202dace56bdf3633cc17464b495bdcc605798`  
		Last Modified: Mon, 22 Sep 2025 23:12:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1571` - unknown; unknown

```console
$ docker pull clojure@sha256:9ada5e5267ef8be7bfa806b7586eaf60edd02f830331d4ede4e01396b737d181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6a8e5d57b45a7425a4743d03345717581be9edc99c1f071af3d17e9e80543`

```dockerfile
```

-	Layers:
	-	`sha256:033371025b522c9acfaa54d091a06142b0f8d326b0193268ae8c7a75bc58a476`  
		Last Modified: Tue, 23 Sep 2025 00:41:29 GMT  
		Size: 7.4 MB (7371311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61b7b22656184524b57bf45b1e14c75e8a59a40e1277dad76fd73220a96664b`  
		Last Modified: Tue, 23 Sep 2025 00:41:30 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
