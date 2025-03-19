## `sapmachine:jre-ubuntu`

```console
$ docker pull sapmachine@sha256:a45dee1ed6c3471c4e3a3646ba4f0f0eb6164f4acb5640d22c6bf628c32486bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:fbc00da57a2a7996567d30d65069edf0b1f200d0d44526a21ca1ef501c94a5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100217058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507ccdb4915f579351d60ecd41626cd5d1f00624a7247d5b3dadd9e1d6c46a39`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ac2f245b9c2ab5a35687fadcce23e1f397d30c8240ce53f1e9561e991b3919`  
		Last Modified: Wed, 19 Mar 2025 20:33:22 GMT  
		Size: 70.5 MB (70462768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4aa87f57b0246c0a9952e537b043d51f0995a3fd71de94547cde7aee8bf4d786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7623f8d49d6f4f7f40fbc3211fd0d0335151abe8e7252bc1e56a611f07bb1eee`

```dockerfile
```

-	Layers:
	-	`sha256:ca911b87f62bfc2176642cc353ca59f9ef73b05d59b9019c884b38ca6401fab9`  
		Last Modified: Wed, 19 Mar 2025 20:33:20 GMT  
		Size: 2.4 MB (2396007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6498649e1971ef71da3218322336cf305d09f6cc65116a8007ed0f8eed3fd95`  
		Last Modified: Wed, 19 Mar 2025 20:33:19 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d6bd86ce2c58ede9a193b7d9e1f0fc68e02608a014d06e2b0113b5e2b3634f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98202572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5c4fef9953627c4969cd024f107c531b9764a85aea9f3ecd4ce3a73794a93f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ec2337e9df053b605df1dc92f6649212c2644797379367e54a159d7fff473`  
		Last Modified: Wed, 19 Mar 2025 20:34:44 GMT  
		Size: 69.3 MB (69308974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ebd72dca411d0b78b7d683d2f18a6a6e641705f1eefaf108ed3a3cb54d9394e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad6e91f3621f5ceb9b57778e49221c76d91d0d67b6c1245c2743f3b7d5535a`

```dockerfile
```

-	Layers:
	-	`sha256:d8fbadcff55c52b49c979149d846fc7bd317e55ab65b763c7461b598fea389bb`  
		Last Modified: Wed, 19 Mar 2025 20:34:42 GMT  
		Size: 2.4 MB (2396496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60108924554ee08863569db454e2cd68b2cb4cfe0eccbd0df5322abc98cc3048`  
		Last Modified: Wed, 19 Mar 2025 20:34:42 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:341a3d9720b0b540a3cb06a620091d61e2553708d8bd0c00fbdba803a919574d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106451833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eb7010f3f3d02a4f5d8775518f6eb4b0b480415a983448893e63cb8ad34f2b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e967e40b52ff51187215c7ed4e69d60bf5ceb5de8059924c9359c15aa587d44`  
		Last Modified: Wed, 19 Mar 2025 20:37:04 GMT  
		Size: 72.1 MB (72062009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05fadf6b9dd36cc968cb6abfc197ea591c6e9fd2235126e7181a21bf39638a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3b44e73488bad2cc5aa80b0ac8f2416d5d61a8a84ef17d4d190ce0f533a8b3`

```dockerfile
```

-	Layers:
	-	`sha256:22c95781e480879328bbc6a37f098ca5c0f00f499ba0dd8993cc02fc8cc79be4`  
		Last Modified: Wed, 19 Mar 2025 20:36:58 GMT  
		Size: 2.4 MB (2399328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f526861641350ca035f162fccc2326550cf31c0802bb26a5b9d910b181097f`  
		Last Modified: Wed, 19 Mar 2025 20:36:58 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.in-toto+json
