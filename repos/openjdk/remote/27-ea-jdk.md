## `openjdk:27-ea-jdk`

```console
$ docker pull openjdk@sha256:254b3d620c4bb30338504e69e618bd14eade7074a16faca884677373b7c686d3
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
$ docker pull openjdk@sha256:0a4b173f7b65421734cf0973f8e312082142b45458f99a1b4dbd5a597eedef7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314036636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb09c1f07a8322992771257e9718fb7f65f8782b7b460f2e877b0ca4cd322b25`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Mon, 16 Mar 2026 17:02:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 16 Mar 2026 17:02:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 16 Mar 2026 17:02:47 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:02:47 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:02:47 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:02:47 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:02:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d9967927c300591059114d76252780f536e22cc379df46d1ff621eb355c32`  
		Last Modified: Mon, 16 Mar 2026 17:03:08 GMT  
		Size: 38.3 MB (38296916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22501fddcb10aa5185d42b18a14029f0d14986fafb40db7c6bc164fa21776fb8`  
		Last Modified: Mon, 16 Mar 2026 17:03:12 GMT  
		Size: 228.4 MB (228435510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:7334640cf4a46bae2d93e0e5f846bbb59694333cdbd7b67ffe7a746f171dfb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36541a3396af40f83e945b4da7b937ae3d9a72aea44329944a3d1e36776430c0`

```dockerfile
```

-	Layers:
	-	`sha256:5695ae08ed8682d99beb822c12ae0d04b7fcb8995fcbae288353309ce371a037`  
		Last Modified: Mon, 16 Mar 2026 17:03:06 GMT  
		Size: 3.7 MB (3655443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2519560bb881b9a27a31c27781edb48d563841d06703e35069a3cf77206322ef`  
		Last Modified: Mon, 16 Mar 2026 17:03:06 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:af1489f3ee73cb15806d002235df45364ecc6902110c85cdf77c4d266d0c8053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (311003869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ff3d9a0e2a649bb303c188d49f1745aeb4f8cfac74c58e4c7ddc6c06c787a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Mon, 16 Mar 2026 17:04:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 16 Mar 2026 17:04:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 16 Mar 2026 17:04:40 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:04:40 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:04:40 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:04:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:04:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3ed50cedf4728d6774eee9a0d38e4258b879d7f673998bb602ecc194fb42f`  
		Last Modified: Mon, 16 Mar 2026 17:05:03 GMT  
		Size: 38.7 MB (38695596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b183a5edc4a023659120338d88516b8e78690d2daa560b9c360bf06929a9ab`  
		Last Modified: Mon, 16 Mar 2026 17:05:07 GMT  
		Size: 226.4 MB (226408087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:07cf699e34644ea1bab35987abd0b1be9e9bff3a04bd006ace7f821235a97567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ad6926d55d1144e611f94460f9a65d152c7c32e6729f4d78067e49ce55ce50`

```dockerfile
```

-	Layers:
	-	`sha256:11a4937652b1c07d32b4e1c0376b81c6e5d8247d2324ecae2a9250cd4df6c0b3`  
		Last Modified: Mon, 16 Mar 2026 17:05:02 GMT  
		Size: 3.7 MB (3653133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c918595c4668d3e34798b27a74ebb7f742152626b08c1e2bda7cbeaabf7978`  
		Last Modified: Mon, 16 Mar 2026 17:05:01 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:163b8f1baf8460cc054b9000909587cce115cc0b9bbea81a6c95ee7cbddfcbfd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306614869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182cf55a2a6122acef220e2ba0f6b1856b471d3320709295d0b670a52c06ed42`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:23 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Mar 2026 22:08:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:29 GMT
ENV JAVA_VERSION=27-ea+12
# Tue, 10 Mar 2026 22:08:29 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:08:30 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Tue, 10 Mar 2026 22:08:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:54 GMT
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
	-	`sha256:9d4b40b53ab8fc04597b6927d1d4100d0966208b15d59e54d372d82c1d5756a9`  
		Last Modified: Tue, 10 Mar 2026 21:59:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fac10204a8f7ab9a2e0d98303da9498677281a47fa131e3e305ea87a1c6850`  
		Last Modified: Tue, 10 Mar 2026 22:09:01 GMT  
		Size: 361.2 KB (361167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a42dec4350ae1fec8a3124d49fe7dab5735247fac6fcc733dd2fa86b8cddd1`  
		Last Modified: Tue, 10 Mar 2026 22:09:00 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cbfb3d9b1b7d0be76aa2a5555453c5cbb795280d007423444398d955cef6ae`  
		Last Modified: Tue, 10 Mar 2026 22:09:01 GMT  
		Size: 338.0 KB (338028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8393dd88d2ecdbbaeecfcb56a0dd5bcf7d87ef5ba3f692f9fef0dbdbe32945`  
		Last Modified: Tue, 10 Mar 2026 22:08:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b219489f31b2c4d18d0d6d4dc9fef6681e0f6f089737777ad059b000c0c0c`  
		Last Modified: Tue, 10 Mar 2026 22:08:59 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69481d98b8c806975a1b933a06c0a331464354140a443d6d2400d7e02002219`  
		Last Modified: Tue, 10 Mar 2026 22:08:59 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393575af8f8f231e5f47cbbbfaf77843473daa353704148a6d01b1a419368b16`  
		Last Modified: Tue, 10 Mar 2026 22:09:14 GMT  
		Size: 224.7 MB (224711857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57e231c4344eb94b3f45aeec4c5a0c759313dd8ab7fbae0e5eadedb9fbe6388`  
		Last Modified: Tue, 10 Mar 2026 22:08:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:31a45f414475b13be910281335a95649582bbe68be8e1cc0a20daa3024b80e95
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207834880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfd5103361edf759fe471582fe5282ee736b0ffddb48552cf02c72a0b1197c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:14:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:14:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Mar 2026 22:15:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:15:01 GMT
ENV JAVA_VERSION=27-ea+12
# Tue, 10 Mar 2026 22:15:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:15:02 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Tue, 10 Mar 2026 22:15:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:15:40 GMT
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
	-	`sha256:f982b44695c6c1cca851e9238aa8eceda2f7522e65a6a1df319239f66b3610fe`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c7ce18d39c8fd66409b6df095755d7331405577028a781dc62022f4be4f7df`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 491.8 KB (491764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9709e89de0f771446b0addeb48003e703cd5533b39b78b867272bbee78b1c7`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b95ef2b220dc5350cda21f1947f8cccb26a0e52134b48ef8a486a531295a7e0`  
		Last Modified: Tue, 10 Mar 2026 22:15:49 GMT  
		Size: 337.9 KB (337886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47e5a03efb8d1c3b42cc3156c2b9730011599ba4962e9e81912ebde2663441d`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5f28235feef5e3517512792b835dcf99ee050da565821b0d860974e9f87d68`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe20410c761248631018d174892c6830bb72938a6d9a926f3df3543dcb71aec`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0c74df48da9f323c40c6c6350831c5c307b337f2349b51479d48d807e1a556`  
		Last Modified: Tue, 10 Mar 2026 22:16:03 GMT  
		Size: 224.7 MB (224715958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b91cbaadd0667bffc39536877ca56f2d47430ee31074c95a6f5cb57f982f65`  
		Last Modified: Tue, 10 Mar 2026 22:15:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
