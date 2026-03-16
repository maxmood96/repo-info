## `openjdk:27-ea-13-jdk`

```console
$ docker pull openjdk@sha256:948cb58c9981d78fccd2fbe1a4633eb91dfef81afbc89240fdf9f36c9d93fc81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-13-jdk` - linux; amd64

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

### `openjdk:27-ea-13-jdk` - unknown; unknown

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

### `openjdk:27-ea-13-jdk` - linux; arm64 variant v8

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

### `openjdk:27-ea-13-jdk` - unknown; unknown

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

### `openjdk:27-ea-13-jdk` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:d88d6743e8d29dc0c94c8c11be2966e986d3a09c3f407721cb081db92a1da1b3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306670912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3034e9f562fc8bc103dd78ef7ef991e355275294246e92581fc735cb0c93cf0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 16 Mar 2026 17:17:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 17:18:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:18:54 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 17:19:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:19:02 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:19:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_windows-x64_bin.zip
# Mon, 16 Mar 2026 17:19:04 GMT
ENV JAVA_SHA256=f5a1c2aa25b826ecdaf3c6614f16bc91e871d38839bf0e01e4e2531bbe590cd0
# Mon, 16 Mar 2026 17:19:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:19:33 GMT
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
	-	`sha256:f6de82b7e7c1f35dde6b4118fb6aebaa42afcb877810f3599bdcd1b4589aaebd`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150d874657d39efabf1e837a905c283aff78878f22caa45276f591804aa1d45b`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 372.8 KB (372821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1a86483f3927a61012f342a7f3a4c40bad7ce19dc61e2a084bfc87c1ee658`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee4aedf713ed51271319bc0e2e93c50a5a781212693c09f0e182daa3bcb849f`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 354.9 KB (354871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623a08f76051a810affcf3626bbdf7e262cf46b5409de42f9445d165443b4b7`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bdbbe743d63a3bd0479c3a83f48b2d59b833f8cad494acd2d15e4156f4d499`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215b3dbc1340d738bd4abec5684d230737b9170dd076e21d39cc637af70dc61`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c059aaeab605e916850f3b272fbbb514a1181ae0bbafc41c3c6a7bb4aa87182`  
		Last Modified: Mon, 16 Mar 2026 17:19:52 GMT  
		Size: 224.7 MB (224739402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf9a17eb23461987ac05549c412d1c12d57af97f774e182c7020011c1dfa62d`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-13-jdk` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:49b37b815e41742fd4fc72935f563e8244b37b1f8cb9b9a915294ed868787b2f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207825888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfbb35e0063895c0089d53f05456bdf0442b68e07ea61c8399a03915fad2d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 16 Mar 2026 18:17:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 18:18:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:18:25 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 18:18:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:18:33 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 18:18:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_windows-x64_bin.zip
# Mon, 16 Mar 2026 18:18:35 GMT
ENV JAVA_SHA256=f5a1c2aa25b826ecdaf3c6614f16bc91e871d38839bf0e01e4e2531bbe590cd0
# Mon, 16 Mar 2026 18:19:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:19:05 GMT
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
	-	`sha256:7495c78820827f6b1f2185c1285dc84d756942187152d024d2e20972fa2b4097`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f97670b4a761ad835ccafbe0a5ccea6a2ccdc7ca02dfe871148832156699fb`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 505.7 KB (505651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0da8f23e7afe73975f1a9e292c93b1682e5bbf47ddeb37121ca776ee991a42a`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c86f8a6a2fe97ffe39cb1345789d861d0d64bdd7f19691afa6b3fe8d2cd5ba`  
		Last Modified: Mon, 16 Mar 2026 18:19:11 GMT  
		Size: 317.5 KB (317534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18c49347be4d99cba7c8ec7789784b904b2f077322192fd65cbd9665a8b6ad`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9327966cec93921a14d4da385f40975c7c8ce35b05add7c279aa67fab2b51bcd`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014def7f2c4de4ac1198a4e015eaa1a8205ab92d7716aa272526247c46adf624`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3cf3feeca970486a1d68f8644dd6dd3e51b6d6ed44d229bd869e55cf945283`  
		Last Modified: Mon, 16 Mar 2026 18:19:25 GMT  
		Size: 224.7 MB (224713478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e49617387eaacfc2f51cac81b4091d275d3368b07678525a6d4ef395f83d658`  
		Last Modified: Mon, 16 Mar 2026 18:19:09 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
