## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:9a37a039e77f4e8f0206a4b5efe2478345e9128861b83f6f96d389eb703302d9
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:03917feaa5478983a37ac136484ad3c0a927c364c82c25506f5f50f36a047a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287489898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce67122a32df3b21809023d34d7faf98d1411af6f2e3a16c3b31c4542f2061f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:05:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:43 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9684646f9122969e5bbb6ed390e3727eec65a66e8810bf6468fdd32c176b7f6`  
		Last Modified: Thu, 05 Feb 2026 23:06:23 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a8a9275a93cfec87ad0556af9b5f2f3a160676702a3cd028d9d3840a6e1134`  
		Last Modified: Thu, 05 Feb 2026 23:06:21 GMT  
		Size: 81.2 MB (81150289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0e0ba149859369744bb56259ea0e1b220ce1cc55606119e61d3c340d7eabc9`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd4c25585ea7d2de9c1be90d003e41daedeeca6d3d21e8cca78b47672a3c83c`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5c9fead09954542383664dbbd12a0a1a440775147354e666467338044105d5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7160c709c62bb3ef15f1e49f7acf0f08dd22426b782864a7fefc573226fef03b`

```dockerfile
```

-	Layers:
	-	`sha256:9a0fd940ae673feaac1e41fc558b2c1b8b2b69189a90d9874695a6ee6c7108a2`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 7.4 MB (7379325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be8c5397732b5bef3f9ad1ee2b1492db955f7b11e4b979ca8b071cbb8218702`  
		Last Modified: Thu, 05 Feb 2026 23:06:18 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65d8c53095207350c4db95a850fe2f5309979d40d6d961ba143724c155e240a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b4c2eca43eb29f9e629307a0ccbb9724dae150a3d42df80ef34e901a2cc381`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:05 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5bea9ae8d0f52b93c4325cca51ebc7b8a1c17148293e178b82c7d22fb56854`  
		Last Modified: Thu, 05 Feb 2026 23:07:46 GMT  
		Size: 156.1 MB (156133062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096bc72b6de72c3161afca95c078a4d2711a253ddac492452b2ad00328e7a5ef`  
		Last Modified: Thu, 05 Feb 2026 23:07:44 GMT  
		Size: 81.1 MB (81137859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45d56dd776c2676704693c65eb0b6fb03cb1d17fe69db6c3a2437a93ed76920`  
		Last Modified: Thu, 05 Feb 2026 23:07:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547956852e6c9a5eef76efff50e453ea52685a40a5cd706f4a2be82752213bfa`  
		Last Modified: Thu, 05 Feb 2026 23:07:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:58a519684e8f08ea0bbf298d261a044b91539df9dbad4c6c0c533215e56993b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5242aa48fd8599bd771b0a136d83d93915c7bdecfe4e40c421ee5fc7c6fe6da`

```dockerfile
```

-	Layers:
	-	`sha256:75db32cddb268bf6f7fea93e363058bbe62a63b68cfdad1f09deb76892956230`  
		Last Modified: Thu, 05 Feb 2026 23:07:42 GMT  
		Size: 7.4 MB (7385112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd4705c11bb96459b5c94c8f81c56bfe0869880c5460bf68b9a939f51009e60`  
		Last Modified: Thu, 05 Feb 2026 23:07:41 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3594f0cd3d8498da4c410d2a7e492a6af600db52be7c2a0cab1bcba56f232957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297292941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043b57a47cb46580e87de3caa01cba610b43a29787e833970fe4b3a0f8369c40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ee00175dff89e342e9299356ae478e81ca394a247a61c2668e6d4d5a094a4`  
		Last Modified: Fri, 06 Feb 2026 00:41:58 GMT  
		Size: 87.0 MB (86987116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f156a5b9e3d97c83ba351ed6f7ac043e2fa92a3e08eabc95e2f5d6eee89ce`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920bf0f293d88423d1c643976512bb472450b1dd8e4f64f7c59eae0376ab4f3`  
		Last Modified: Fri, 06 Feb 2026 00:41:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:934fec4a17685b03f9687a4dc08f44e31290224fa8353e92c091a4bbc634d736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e884b1738899f776ba80cffc28d38301a5d8b1ebc1bcfa41a617a14299fdefc`

```dockerfile
```

-	Layers:
	-	`sha256:c67e5415aa8ba7b167623375f77299806bfe62df447da3aad5c97b2317e515e3`  
		Last Modified: Fri, 06 Feb 2026 00:41:56 GMT  
		Size: 7.4 MB (7384553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6d1f76d5e550ef7ad37e90f071c56e740b96fe02063bf5d167ca30463179fa`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0cc35ffab0d789035f21b94dda2202e679e158bfe78d85621b0a3779f3f55a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274207578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db498030ac2f2b73ef6e0fbbbf7f2f0d1c9fcb6bfcae7c93fbba1c4e0610dd7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:43 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87516b64b39f17ace7ef42f2534985c89459dec5eb2b0d78d5e5ea2b52e133`  
		Last Modified: Thu, 05 Feb 2026 23:07:32 GMT  
		Size: 147.1 MB (147105286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7bb380abf1a95b9ba847fff28f9df7ef8f1da904fa04a60304281d8e794642`  
		Last Modified: Thu, 05 Feb 2026 23:07:30 GMT  
		Size: 80.0 MB (79962909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de31f432941fdb774e9ab125bf1dd29f34fc3bcd2bdc51caf4fc3b4cf7072ab7`  
		Last Modified: Thu, 05 Feb 2026 23:07:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5b969fca9610900da426962afc4359c0d906dbb0ecc8ca1322d5ed38f2bd5`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4642e16d4648fd5d8ed13c479cd6385431ec889e5a123964daa278685105176f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6949423abf2f2a9065eef6e34b247bd99e52641b046c45e21fc15133944e9c08`

```dockerfile
```

-	Layers:
	-	`sha256:2ca028c9918cd997e56d3c7f5c1540c11d452d7b0f8815b7d542cb42e030a5b6`  
		Last Modified: Thu, 05 Feb 2026 23:07:28 GMT  
		Size: 7.4 MB (7370644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf4e3ffcb92bb36ad5d41be16054ccdc335f27e1d7ac809d1d9a915afafbf18`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
