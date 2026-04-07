## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:5a4d244c19d25ee2df962b6c0a496e580c02fe424e18e7bedd50bf54c2321787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3fd24a3628c9f11410908bade3481cedb4d4f834ff791cbab5166c3734a87c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309539871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eeb6291d69d56c3815374146a66a8d59077a8f7bcb074b8c9f708cb292c678`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:24:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:24:40 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:24:40 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:24:40 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:24:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:24:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1101a6a16bdd51aef6dda35e785dca1d7934d2937fdc0c8dfc0f002ced99f85a`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 43.1 MB (43068827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bad064764c9cdc9f064864f294e76ab15178c55145f51897ee66cc9a58111`  
		Last Modified: Mon, 06 Apr 2026 18:25:01 GMT  
		Size: 37.7 MB (37679171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac96a95ecb13c0123ebe6a94f0b7592bbc861fc6c5652a71e911b147fdee87d`  
		Last Modified: Mon, 06 Apr 2026 18:25:05 GMT  
		Size: 228.8 MB (228791873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4e56747123c8003d1c5c3e7128f433a757a205cface8b813824ecbb6ce07e966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1059e6b0e357a06004d423d83c2cd695d2ff6c7494626533690b56dc8138c231`

```dockerfile
```

-	Layers:
	-	`sha256:3f7b6d823671076efd86874b8bf81ecc33d75101b8241c1099088246c6d7a4a3`  
		Last Modified: Mon, 06 Apr 2026 18:25:00 GMT  
		Size: 2.4 MB (2368347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6801b2e257ab885cb45ac11b3ef304a84afab23dbf50a074262d05be9e8d9687`  
		Last Modified: Mon, 06 Apr 2026 18:25:00 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1367fdbec048916da4316d05cb03e2041c6b9a15eb32dcb2b6018cc3c43cb3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305921504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f26de63ec08cb96d36e67a76ab20ad3d2d6f213deb91536c8d440194f8755d4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:24:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:24:33 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:24:33 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:24:33 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:24:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:24:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3db22c05661dd4dd65ed2c3add4946b3292ef86d7a62c06699ee25367fc2e1b`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 41.5 MB (41474500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169191e7a1b452ded0d6b5c4b4881bba8e3bae3cca641b8ec2114e4bd4d73035`  
		Last Modified: Mon, 06 Apr 2026 18:24:56 GMT  
		Size: 37.7 MB (37687605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2e7c0d3a615ae73ae254a6cc2272cab7f6cffd7bf90de7b69393ae67986489`  
		Last Modified: Mon, 06 Apr 2026 18:25:01 GMT  
		Size: 226.8 MB (226759399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:0e92a901ea2f92ebc102f75f9af8bbe4815fb86a70b63197e973c39263e8cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8d5861d6b9a28db8cc8f049278c6c0aa31e463113cdf502403160f76927fd9`

```dockerfile
```

-	Layers:
	-	`sha256:015aac055b5b0f7438c987a86de22d4a81e78783147868f4fbfd29959b18fcdd`  
		Last Modified: Mon, 06 Apr 2026 18:24:55 GMT  
		Size: 2.4 MB (2367875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb6e5e807ab37a84a4cbb1caee9d349fcabc383a41d895f285a775b495cb7d0`  
		Last Modified: Mon, 06 Apr 2026 18:24:55 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:26e06e40e8a0cecdc4e509e0b829efae6c8496b0aa9eed3e9e7afe5f6446da0e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2307108797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8570d771ed3a0584de0ff1ce1ff9598208de75790b6c25f1a315118c58645038`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 06 Apr 2026 18:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Apr 2026 18:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:19 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:27:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:27 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:27:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_windows-x64_bin.zip
# Mon, 06 Apr 2026 18:27:29 GMT
ENV JAVA_SHA256=e5c718947519c88a2ee3b23aea3ed1da5b81b674c4f03fe8b29395ab126d36ef
# Mon, 06 Apr 2026 18:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:28:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7157efab2f341875530685270a8e3ebd68d46fce725e5023b31f0ab24bff80`  
		Last Modified: Mon, 06 Apr 2026 18:28:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609aaed14f2f94e01ab3704870a1faa711744e29a7b05512e7bd7e25f5989eaa`  
		Last Modified: Mon, 06 Apr 2026 18:28:35 GMT  
		Size: 388.1 KB (388057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9773285db393376a2da37442199f23b414c9b2789c64e40616b6d2009b2e7eb`  
		Last Modified: Mon, 06 Apr 2026 18:28:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a247f5112c541e9a7326e4a8ebd607f035883872d142c077bf185237f3a2f05`  
		Last Modified: Mon, 06 Apr 2026 18:28:35 GMT  
		Size: 369.8 KB (369774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8adf67f58f5f31c6d1ab31ad6488ceabaf57de5137a53c4978adc565127d28`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057362a51559414a1bf3bbb6adafeab82ad9e9beed098fb2206cb097201fb009`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb8e536e0a07f45ea489905239d15cc2e99cc27219c82aba97c233c2e54568`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0395289ca06d1f4ef950720934332cba4b8360c360c6a96907379c1d3fb99bf6`  
		Last Modified: Mon, 06 Apr 2026 18:28:49 GMT  
		Size: 225.1 MB (225147060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56253a51a86d37d215981a3c700e73e0b606af875fa0cd11e100a2244a6239c2`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:eb45b67eedd2803108228b7d138f1734ea1f42063f5329a377a22749b6bbbfdb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2208196475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375ceea08424f1c4ed435d91153a165b9ece980ff59ad6a3a0c4d3924bcc7fa8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 06 Apr 2026 18:26:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Apr 2026 18:27:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:42 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:27:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:51 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:27:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_windows-x64_bin.zip
# Mon, 06 Apr 2026 18:27:54 GMT
ENV JAVA_SHA256=e5c718947519c88a2ee3b23aea3ed1da5b81b674c4f03fe8b29395ab126d36ef
# Mon, 06 Apr 2026 18:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:29:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72fc8f6d3e1f9d440258f21d8669b9f0aacd885e9cd5dca2fa0d7efc6b5ca90`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1553d29986a9afb26d4654683f1640f6f5f4f5a1637762f21ea6bd52ff4eb2`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 505.9 KB (505856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc798538ff19391e156cfcfcf19134db65f1e7df7a15398665449f507ec0f6fe`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657fb46d0888e2aa30abce440e4032931b2529f37b54c8463f7310a72501d79`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 305.2 KB (305152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f805fdce7eec62bf36217cfd5f5ed02496dd69856c4f98f613cb8031b0dc6`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefd9ec11c6c5e977745bd6d4906d7d8cc642ebe011af12ee7a9ec283e776f78`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b71f33cf29a9362f6eb1f8279aed2d8fed2752ba4f501b5f0a30592b121a502`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627d952d69a2940a1429a6cbdfd79099f24b6b31fecba88395849e0349d83293`  
		Last Modified: Mon, 06 Apr 2026 18:30:14 GMT  
		Size: 225.1 MB (225096230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0deca905a948981090dfd879486816c4e6e4e61185951e3290595eaae9145`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
