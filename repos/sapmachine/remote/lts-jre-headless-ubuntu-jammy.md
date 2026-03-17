## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:15abee2082374d3a7fbd14a9cc5f225e4e6b087c21a9e3dd3c9a25b969816758
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:90710a71a09b2a3b3258a3d795de9f773adc61d33f26edde1cd57d9fa7913d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85666919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f945e7e7f84c98156b7ebabbc528ad45e2fcab09ad6379ce79d5c81e4db3a4ec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:24:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f820dde4ffac811b9dc488efe2c179a2f7f721ffb1ec3072c348ce257c42ebc`  
		Last Modified: Tue, 17 Mar 2026 02:24:22 GMT  
		Size: 56.1 MB (56128399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e1cd95d7bdb02e1f8470b1f1d57411c0fd38972e0e36730d576601d4eea23dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3165252e526ad41f5b441ed6c0950acc021235a9a02db894c8095c64a9cc1d1`

```dockerfile
```

-	Layers:
	-	`sha256:b47fb66fa2d2177540eeae8458c0766523007a2f6af3817344bc9a1f611bb018`  
		Last Modified: Tue, 17 Mar 2026 02:24:20 GMT  
		Size: 2.3 MB (2303043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a4b9c0f25f44e133e48fb057bda90841fc38a670e01dc3a3f9f9eea4710d64`  
		Last Modified: Tue, 17 Mar 2026 02:24:20 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1ebe7d0614b7787b42acb2c8e2b7d48a0323c299bde9c476ef8021d0a2c7921c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82435253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c39106c165cb1d71ba072ff5cd74c909544d7c5c2e1d5d3ed7b447500871ac7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:30:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:30:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d3b74593352c23c69506216e65baf6e8f120ecd444f8bb7ee9f00d33192c91`  
		Last Modified: Tue, 17 Mar 2026 02:30:28 GMT  
		Size: 55.0 MB (55046228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd7f65929138e62f8565b22b059179a8748650c0bcd3748255ded71f0c4d5f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c9d66037c846a33eec045174b838ab105f5ef8e999183241ae89d98812960e`

```dockerfile
```

-	Layers:
	-	`sha256:cd7f962a904f4e460836ba5b40a087ff9c5f35d8612371f044dd9df4db0e422b`  
		Last Modified: Tue, 17 Mar 2026 02:30:26 GMT  
		Size: 2.3 MB (2302760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8715ba39ab4848ca7b45777cb52e6572997ee0ad597c05c0a5622e5f8a8cb6c`  
		Last Modified: Tue, 17 Mar 2026 02:30:26 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d66fb72125132669b0550aa234d57553c1d37a620bfec60a9b098fceb38c9ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91279320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e414850b5557f2f1181b7687cbfed54499634b625518a08f351690c7c58e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 00:14:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 00:14:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 18 Feb 2026 00:14:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db9f21078af57cff3c0a036a940c5bd45942d6e11dc0d7d7f32e280f4fa3b72`  
		Last Modified: Wed, 18 Feb 2026 00:15:13 GMT  
		Size: 56.8 MB (56833218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d68e08e27f2880b911f567a39cfbfaec90ef5a8167c1c63851062bfaa8060cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a1a655868cceae1740750141eafe048229bfcc3ba6c799f981e4a353dd53a`

```dockerfile
```

-	Layers:
	-	`sha256:d0d129f2bd0c8fbe8ef93a3ba0218af9a10fdef7b650002dec02f2ff8c1f1a09`  
		Last Modified: Wed, 18 Feb 2026 00:15:11 GMT  
		Size: 2.3 MB (2301879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3b5945a7aa071bf74d7975a33c5983d01c105bcf64e2d54cc8c67f13054cee`  
		Last Modified: Wed, 18 Feb 2026 00:15:11 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
