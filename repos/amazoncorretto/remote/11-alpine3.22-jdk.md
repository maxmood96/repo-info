## `amazoncorretto:11-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:7a3642d89a4b62332f565071c095a509957965155cf57a46b2da2c307b212282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:605c4719adc63ade75e5ce0596fb5a8c54e7c4901e3e88348ff862dc8af5042a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147497186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0682d87f5e7be75cd5be8b4c9415e656270c76d7bbc20c22c02c2e05f94518`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:36 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:36 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d550004943d1fc4abb470a4cf28bbe7468922b3cb35269b870dee98117ca6076`  
		Last Modified: Wed, 22 Apr 2026 21:33:53 GMT  
		Size: 143.7 MB (143688997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:389b93bee35f29d95d484e2b6aad1ae45def67ff471c38190b050de63525f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b751519e9d3e762c9d4fb5251065259e0e75a40129082d197580b88a7fbb5840`

```dockerfile
```

-	Layers:
	-	`sha256:f8d81ac93e56b4984bdc5c6585e62cb1bb35075bc49f1977431d0176cfeadce1`  
		Last Modified: Wed, 22 Apr 2026 21:33:50 GMT  
		Size: 588.9 KB (588930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331459cd55a6e2f021157f9239438dcf0475303471a08bd0f38cc56c3cc3c296`  
		Last Modified: Wed, 22 Apr 2026 21:33:49 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:24ca3b49d6ee1fcf113d63b29bebb9548be65e958dbafc7d6e3ccbfa9de4f3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146103263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62e22cd378f10580f29ff4c444429460b244648f937bb2a1487f40e9803f2d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:31 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:31 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:31 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82af60a2f3edf58ce934238b0667e8d9798280c5a44e812cf7962ee71b05b311`  
		Last Modified: Wed, 22 Apr 2026 21:33:51 GMT  
		Size: 142.0 MB (141961369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f07c81e55cd425503b3129167ad94e05a0b39202275201b9b84a6bf51b69476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3596cfbd210eaf463c06df7b19eb803df0606a7361809d1cc9cc3e81b3965bc8`

```dockerfile
```

-	Layers:
	-	`sha256:5ec19e171d44ef48e7d29692524a84f0c430d09ed68a340e0a5ed942386cc631`  
		Last Modified: Wed, 22 Apr 2026 21:33:46 GMT  
		Size: 589.0 KB (588986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb4d8978e5c9bb027f89015816519b87818b99f9fff77e318cb86819d24e48d`  
		Last Modified: Wed, 22 Apr 2026 21:33:46 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
