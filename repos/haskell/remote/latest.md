## `haskell:latest`

```console
$ docker pull haskell@sha256:98122249fcb1c9ea16c77cd8827c1b80b2fb39a5d3a8f2ce2126e441912b0fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:348ba955e8178c9a0175b94e21dd1f2134ec6244941f4c5eb837c98fb91a7587
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.9 MB (412881185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1b7d7d9529d1332e358e1eca71e23a15b2f80730126b3aca3d5faf93fffa83`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 08:52:11 GMT
ENV LANG=C.UTF-8
# Tue, 23 Nov 2021 22:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 Nov 2021 22:29:30 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 23 Nov 2021 22:29:30 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 23 Nov 2021 22:29:30 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=4759B56E9257E02F29FA374A6B25D6CB2F9D80C7E3A55D4F678A8E570925641C
# Tue, 23 Nov 2021 22:29:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=4759B56E9257E02F29FA374A6B25D6CB2F9D80C7E3A55D4F678A8E570925641C
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux-deb10.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:29:42 GMT
ARG GHC=9.2.1
# Tue, 23 Nov 2021 22:29:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 23 Nov 2021 22:29:42 GMT
ARG GHC_RELEASE_SHA256=53F1650ED092230480FF5750B94F409E5DFE66BD07CED00BBBCDF5D6B180234C
# Tue, 23 Nov 2021 22:30:56 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=4759B56E9257E02F29FA374A6B25D6CB2F9D80C7E3A55D4F678A8E570925641C GHC=9.2.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=53F1650ED092230480FF5750B94F409E5DFE66BD07CED00BBBCDF5D6B180234C
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Tue, 23 Nov 2021 22:31:00 GMT
ARG STACK=2.7.3
# Tue, 23 Nov 2021 22:31:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 Nov 2021 22:31:01 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Tue, 23 Nov 2021 22:31:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=4759B56E9257E02F29FA374A6B25D6CB2F9D80C7E3A55D4F678A8E570925641C GHC=9.2.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=53F1650ED092230480FF5750B94F409E5DFE66BD07CED00BBBCDF5D6B180234C STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Tue, 23 Nov 2021 22:31:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Nov 2021 22:31:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a20868c05df53bef0e6cda140c04aa44d362d19059dfc32f79ebede81719e8`  
		Last Modified: Tue, 23 Nov 2021 22:31:57 GMT  
		Size: 117.1 MB (117078249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e79aff48898507e28f32e7273f02c626509647b2d30f981bdf52a54914f164`  
		Last Modified: Tue, 23 Nov 2021 22:31:42 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137b29de7ea53c122e6058402aa59d70ab2761020fca0a34aae9d14cd0ed1b3d`  
		Last Modified: Tue, 23 Nov 2021 22:32:25 GMT  
		Size: 217.4 MB (217432308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a36eb77609b04e2fcd3d805eab862fcfdc36f465bdea1e7eddeff5b515ff7d`  
		Last Modified: Tue, 23 Nov 2021 22:31:44 GMT  
		Size: 17.9 MB (17901260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
