## `sapmachine:17-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:e0077ec5cfca9409673c8ef4d34655503dea4c54d62fd6d8be64cb53b42442c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:79df8725d4fb9a2f12be4fe656ea848fe5477613229a7c05370859682913e7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230121526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073adbf095fc3122eb234ee37ba462c4f40ad23ce6811bf7d65b53643630d57d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d23fe4cb1f8a503cfeedaca2f49ab3f4105eb61a22f26672589446b53bb7f`  
		Last Modified: Mon, 05 May 2025 16:37:10 GMT  
		Size: 200.4 MB (200403997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:81ecc967bc2a8e290c9e85ea848f0cb81399ca23de013a99c09a87d1b50c44ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15394819fe25f0e7a82b2605051f2cc29a267973e2628c892c760345cad308b`

```dockerfile
```

-	Layers:
	-	`sha256:8700285add478ba77df98f806f28696421347503756a696ffc0f71ec5d5a2735`  
		Last Modified: Mon, 05 May 2025 16:37:07 GMT  
		Size: 2.5 MB (2470414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f956ec0d202adf6170d3029cc90f7d361be6f040636d04589b8d09f48a22882`  
		Last Modified: Mon, 05 May 2025 16:37:07 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3312eaa55f1d721d8b54ecac15a66723fa52ba8045fb0c6720f60f855e4a706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228006095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a196d7334635384d6b777c416c80b0e977a8fc5cbcfd3ed6f7da2c15717df9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9c9fefc1100f934e0d675fe4f1f236de9394738bfa7433a6c8b1c81dca26e5`  
		Last Modified: Mon, 05 May 2025 18:38:14 GMT  
		Size: 199.2 MB (199159219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2536c6da0ecf7b931c6029613d02a3b2467b022f20eba2ca74e28dc80f6f4b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2482571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b514d7a6d55555c749b0d11d308664cd47fc0954b03008f6d0a6f8fc9a8d1e6`

```dockerfile
```

-	Layers:
	-	`sha256:2a359f44c2da4d7f01a8fabf4cb93d09272e3eb803e6878252d16d07a78dacc6`  
		Last Modified: Mon, 05 May 2025 18:38:08 GMT  
		Size: 2.5 MB (2470978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c9990e0e6bde2db9a552a5768893a1013a336668abf1fd54eed5d44f00b87f`  
		Last Modified: Mon, 05 May 2025 18:38:07 GMT  
		Size: 11.6 KB (11593 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b1dac5432a80c0254d0b69c8e18e0289791b7457e547a3051f147424c1d46d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235932023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec337b8c3927bf52e862f06b0490f4d4b15ae006673698cff8378d55601dcc1c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69427780a28db3400fb5f722fd874218a1e1c8f828989110e359590c7b26cbd8`  
		Last Modified: Mon, 05 May 2025 18:33:52 GMT  
		Size: 201.6 MB (201591185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:146a395aa5d5591a2867c5ab5e810258b6e4264dba9891fbd47e92f77488a042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895dd89e8d074ddab16a42684badb4aa17a6f4e1b3dd9d2e13045006239a9e82`

```dockerfile
```

-	Layers:
	-	`sha256:7c450641d87cd8a477a010db6e86d77bb93bc2382cef0171928a542d194ff080`  
		Last Modified: Mon, 05 May 2025 18:33:47 GMT  
		Size: 2.5 MB (2472455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0df4197f277ae3fb809edd7e43bfe9c237aedcf35f3b85570d05f3173508d1e`  
		Last Modified: Mon, 05 May 2025 18:33:46 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json
