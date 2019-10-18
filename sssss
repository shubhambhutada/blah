public void setNewCreditPin(BigInteger creditCardNumber, int newPin) {
		// bean1 = creditCardDetails.get(creditCardNumber);
		// bean1.setCreditCurrentPin(newPin);
		// creditCardDetails.replace(creditCardNumber, bean1);
		String sql = SqlQueries.SET_CREDIT_CARD_PIN;
		try (Connection connection = ConnectionProvider.getInstance().getConnection();
				PreparedStatement preparedStatement = connection.prepareStatement(sql);) {

			preparedStatement.setInt(1, newPin);
			preparedStatement.setBigDecimal(2, new BigDecimal(creditCardNumber));
			preparedStatement.executeUpdate();

			
		} catch (Exception e) {
			e.printStackTrace();
		}

	}
