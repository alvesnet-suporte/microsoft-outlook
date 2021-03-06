# microsoft-outlook

fonte: https://docs.microsoft.com/pt-br/outlook/troubleshoot/data-files/file-size-limits-of-pst-and-ost-files-are-larger

# Os limites de tamanho de arquivo de arquivos .pst e .ost são maiores no Outlook 2010 e no Outlook 2013
09/04/2021

Aplica-se a:
Outlook 2013, Microsoft Outlook 2010
Número KB original:   982577

# Introdução

Por padrão, pastas pessoais (.pst) e arquivos do Arquivo de Dados do Outlook offline (.ost) estão no formato Unicode no Microsoft Outlook 2010 e no Outlook 2013. O tamanho geral dos arquivos .pst e .ost tem um limite pré-configurado de 50 GB. Esse limite é maior do que o limite para arquivos .pst e .ost Unicode no Outlook 2007 e no Outlook 2003.

 # Observação

O novo limite de tamanho de arquivo do Outlook de 50 GB pode ser aumentado ou reduzido fazendo alterações no Registro do Windows. Para obter mais informações, consulte Como configurar o limite de tamanho para arquivos (.pst) e (.ost) no Outlook.

fonte: https://support.microsoft.com/pt-br/topic/como-configurar-o-limite-de-tamanho-para-arquivos-pst-e-ost-no-outlook-2f13f558-d40e-9c2a-e3b6-02806fa535f4

# Como configurar o limite de tamanho para arquivos (.pst) e (.ost) no Outlook

# Resumo

O Microsoft Outlook 2016, o Outlook 2013, o Outlook 2010, o Outlook 2007 e o Outlook 2003 dão suporte a arquivos de pastas pessoas (.pst) e a arquivos de pastas offline (.ost) ANSI (American National Standards Institute) e UNICODE. Este artigo descreve como usar as quatro entradas do Registro a seguir para limitar o tamanho dos arquivos .pst e .ost:

A entrada do Registro MaxFileSize

A entrada do Registro WarnFileSize

A entrada do Registro MaxLargeFileSize

A entrada do Registro WarnLargeFileSize

Observação As entradas do Registro WarnLargeFileSize e WarnFileSize não habilitam o Outlook para avisá-lo antes que o limite de tamanho de arquivo seja atingido.

# A entrada do Registro MaxFileSize

A entrada do Registro MaxFileSize determina o tamanho máximo absoluto que os arquivos .pst e .ost podem alcançar. Após esse tamanho máximo ser alcançado, o Outlook não permite que o tamanho de arquivo cresça além desse tamanho.

# A entrada do Registro WarnFileSize

A entrada do Registro WarnLargeFileSize determina o número máximo de dados que os arquivos .pst e .ost podem ter. Após o número máximo de dados ser alcançado, os arquivos .pst ou .ost não podem adicionar mais dados. Entretanto, o tamanho de arquivo físico talvez ainda possa ser aumentado devido a processos internos.

Na tabela a seguir, as do Registro MaxLargeFileSize e WarnLargeFileSize se referem a um arquivo formatado em UNICODE (novo formato Large), enquanto as entradas do Registro MaxFileSize e WarnFileSize se referem a um arquivo formatado em ANSI (um formato anterior do Microsoft Outlook). Os valores UNICODE são definidos em incrementos de MB, enquanto os valores ANSI são definidos em incrementos de byte.

<p align="center">
    <img src="/outlook-tabela1.png" width="724" height="324">
</p>

<p align="center">
    <img src="/outlook-tabela2.png" width="724" height="324">
</p>

# Versão do Office

# 1. Outlook 2013

# O local da diretiva para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\15.0\Outlook\PST

# O local de preferência do usuário para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\PST

# 2. Outlook 2010

# O local da diretiva para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\PST

# O local de preferência do usuário para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Outlook\PST

# 3. Outlook 2007

# O local da diretiva para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\12.0\Outlook\PST

# O local de preferência do usuário para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Microsoft\Office\12.0\Outlook\PST

# 4. Outlook 2003

# O local da diretiva para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\11.0\Outlook\PST

# O local de preferência do usuário para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Microsoft\Office\11.0\Outlook\PST

# 5. Outlook 2016

# O local da diretiva para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\16.0\Outlook\PST

# O local de preferência do usuário para entradas do registro está localizado no seguinte caminho no Editor do Registro

HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\PST
